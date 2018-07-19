
<template>
  <div>
      <h1>姓名：{{info.name}}</h1>
      <h2>年龄：{{info.age}}</h2>
      <h2>兴趣：{{info.interest}}</h2>
      <!-- <p>{{sex}}</p> -->
  </div>
</template>
<script>
import axios from 'axios'  // 这种方式的话 如果在别的页面也用到这个插件，会被打包多次。  解决方式 去  nuxt.config.js 里面配置 build.vendor 来解决：
export default {
  data(){
     return {
         name:'hello World',
         info:{}
     }
  },
  async asyncData(){  // nuxt的异步获取数据方法
    let {data} = await axios.get('https://api.myjson.com/bins/8gdmr')
    return {info: data ,sex: 'male'}
  }
  // async created () {  // 这种 就没  SSR 效果
  //   let {data} = await axios.get('https://api.myjson.com/bins/8gdmr')
  //   this.info = data
  // }
}
</script>
