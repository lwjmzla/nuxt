<template>
  <section class="container">
    <div>
      <div class="diss"  @click="$store.commit('increment')">
        <img src="~static/logo.png" />
        {{ $store.state.counter }}
      </div>
      <ul>
        <li><nuxt-link :to="{name:'index'}">HOME</nuxt-link></li>
        <li><nuxt-link :to="{name:'about',params:{id:1}}">ABOUT222</nuxt-link></li>
        <li><nuxt-link :to="{name:'news',params:{id:1}}">news</nuxt-link></li>
        <li><nuxt-link :to="{name:'ansyData'}">ansyData</nuxt-link></li>
      </ul>
    </div>
  </section>
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'

export default {
  components: {
    AppLogo
  }
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  height: 2000px;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
.diss{
  width: 300px;
  height: 300px;
  background: url('~static/icons.png') no-repeat center center red;
}
.diss img{transform: rotate(90deg);}
</style>
