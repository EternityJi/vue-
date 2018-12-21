<template>
  <div>
    <!-- home-header ==> HomeHeader  vue会自动拆分 -->
    <home-header></home-header>
  </div>
</template>
<script>
// 局部组件
import HomeHeader from './components/Header.vue'
export default {
  name: 'Home',
  components: {
    HomeHeader
  }
}
</script>
<style>
</style>
