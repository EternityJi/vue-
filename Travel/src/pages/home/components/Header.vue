<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe622;</div>
    </div>
    <div class="header-input"><span class="iconfont">&#xe819;</span> 输入城市景点游玩主题</div>
    <div class="header-right">城市
      <span class="iconfont arrow-icon">&#xe64a;</span>
    </div>
  </div>
</template>
<script>
export default {
  name: 'HomeHeader'
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl';

.header {
  display: flex;
  line-height: 0.86rem;
  height: 0.86rem;
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

    .arrow-icon {
      margin-left: -0.04rem;
      font-size: 0.24rem;
    }
  }
}
</style>
