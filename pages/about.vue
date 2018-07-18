<template>
  <div>
    about
    <p>id:{{$route.params.id}}</p>
  </div>
</template>

<script>
  export default {
    data () {
      return {

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
    transition:'test'  // 该页面才有的 动画效果
  }
</script>

<style scoped>
  div{color: aqua;}
  .test-enter-active, .test-leave-active {
      transition: all 2s;
      
  }
  .test-enter, .test-leave-active {
      opacity: 0;
      font-size:40px;
  }
</style>
