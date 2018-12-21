<template>
  <div>
    <!-- home-header ==> HomeHeader  vue会自动拆分 -->
    <home-header></home-header>
    <home-swiper></home-swiper>
  </div>
</template>
<script>
// 局部组件
import HomeHeader from './components/Header.vue'
import HomeSwiper from './components/Swiper.vue'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper
  }
}
</script>
<style>
</style>
