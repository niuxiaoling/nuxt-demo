<template>
  <div>
    <h2>news page</h2>
    <!-- <p>newsiD：{{$route.params.newsiD}}</p> -->
    <ul>
      <li>
        <nuxt-link :to="{name:'index'}">Home</nuxt-link>
      </li>
      <li>
        <nuxt-link :to="{path:'/news/123'}">news-1</nuxt-link>
      </li>
      <li>
        <nuxt-link :to="{name:'news-newdetail',params:{newdetail:'fff'}}">news-32</nuxt-link>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data () {
    return {
      title: '新闻页面'
    }
  },
  head () {
    return {
      title: this.title,
      // meta: [
      //   { hid: 'description', name: 'description', content: 'befautiful girl' }
      // ]
    }

  }
}
</script>
