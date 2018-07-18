<template>
  <div>
    news
    <p>idddddddd:{{$route.params.numid}}</p>
  </div>
</template>

<script>
  export default {
    data () {
      return{
        title:this.$route.params.title,
      }
    },
    components: {

    },
    beforeRouteEnter (to, from, next) {
      console.log(to)
      console.log(from)
      console.log(next)
      next()
    },
    validate ({ params }) {
      // Must be a number
      return /^\d+$/.test(params.numid)   // 这个正则 的意思 是先校验 参数 ，是数字 才 显示 否则404
    },
    //独立设置head信息
    head(){
      console.log(1)
      return{
        title:this.title,
        meta:[
          {hid:'description',name:'description',content:'This is news page'},
          {hid:'keywords',name:'keywords',content:'news-key'}
        ]
      }
    }

  }
</script>

<style>

</style>
