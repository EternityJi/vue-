<template>
  <div class="header">
    城市选择
    <router-link to="/">
    <div class="iconfont back-icon">&#xe622;</div>
    </router-link>
  </div>
</template>
<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang='stylus' scoped>
@import '~styles/varibles.styl'
.header {
  overflow: hidden;
  height: $headerHeight;
  line-height: $headerHeight;
  text-align: center;
  color: #fff;
  background:  $bgcolor;
  font-size: .32rem
   .back-icon{
      width: 0.64rem;
      float: left;
 text-align: center;
  font-size: .4rem
      color: #fff
   }
}
</style>
