<template>

  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe622;</div>
    </div>
    <div class="header-input"><span class="iconfont">&#xe819;</span> 输入城市景点游玩主题</div>
    <router-link to="/city">
    <div class="header-right">{{ this.city }}
      <span class="iconfont arrow-icon">&#xe64a;</span>
    </div>
    </router-link>
  </div>
</template>
<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl';

.header {
  display: flex;
  line-height: $headerHeight;
  height: $headerHeight;
  background: $bgcolor;
  color: #fff;

  .header-left {
    width: 0.64rem;
    float: left;
    text-align: center;

    .back-icon {
      text-align: center;
    }
  }

  .header-input {
    flex: 1;
    padding-left: 0.2rem;
    height: 0.64rem;
    line-height: 0.64rem;
    margin-left: 0.2rem;
    margin-top: 0.12rem;
    background: #fff;
    border-radius: 0.1rem;
    color: #ccc;
  }

  .header-right {
    width: 1.24rem;
    float: right;
    text-align: center;
    color: #fff

    .arrow-icon {
      margin-left: -0.04rem;
      font-size: 0.24rem;
    }
  }
}
</style>
