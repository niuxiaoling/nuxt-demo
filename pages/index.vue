<template>
  <section>
    <ul>
      <li>
        <nuxt-link :to="{name:'index'}">Home</nuxt-link>
      </li>
      <li>
        <nuxt-link :to="{name:'about',query:{id:123}}">about</nuxt-link>
      </li>
      <li>
        <nuxt-link :to="{name:'news',params:{newsiD:'111'}}">news</nuxt-link>
      </li>

    </ul>
    {{info.name}}
  </section>
</template>

<script>

import axios from 'axios'
export default {
  components: {
  },
  data () {
    return {}
  },
  // 在渲染组件之前异步获取数据
  async asyncData () {
    let { data } = await axios.get('https://api.myjson.com/bins/80woi')
    return { info: data }
  }
}
</script>

<style>

</style>
