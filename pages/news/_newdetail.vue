<template>
  <div>
       <h2>news page</h2>
        newsid: {{$route.params.newdetail}}
    
  </div>
</template>
<script>
export default {
  validate ({ params, query }) {
    return /^\d+$/.test(params.newdetail)
  },
  data () {
    return {
      title: '详情页'
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

<script>
export default {
  transition:'test'
}
</script>
