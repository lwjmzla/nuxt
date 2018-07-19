<template>
  <div class="news">
    news
    <p>newsid:{{$route.params.id}}</p>
    <ul>
      <li><nuxt-link :to="{name:'news-numid',params:{numid:11,title:'jking11'}}">news1</nuxt-link></li>
      <li><nuxt-link :to="{name:'news-numid',params:{numid:12,title:'jking12'}}">news2</nuxt-link></li>
    </ul>
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
    layout: 'blog',
    asyncData () {
      window.scrollTo(0,0);
    }
  }
</script>

<style scoped>
  .news{height: 2000px;}
</style>
