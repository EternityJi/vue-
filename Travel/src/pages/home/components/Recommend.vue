<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item"
          v-for="item in list"
          :key="item.id"
          border-bottom>
        <div class="item-img-wrapper">
          <img class="item-img"
               :src='item.imgUrl'
               alt="">
        </div>
        <div class="item-info">
          <div class="item-title">{{ item.title }}</div>
          <div class="iten-desc">{{ item.desc }} </div>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>

export default {
  name: 'HomeRecommend',
  props: {
    list: Array
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/mixins.styl';

.title {
  margin-top: 0.2rem;
  line-height: 0.8rem;
  background: #eee;
  text-indent: 0.2rem;
}

.item {
  overflow: hidden;
  display: flex;
  height: 1.9rem;

  .item-img {
    width: 1.7rem;
    height: 1.7rem;
    padding: 0.1rem;
  }

  .item-info {
    flex: 1;
    padding: 0.1rem;
    min-width: 0;

    .item-title {
      line-height: 0.54rem;
      font-size: 0.32rem;
      font-weight: 700;
      ellipsis();
    }

    .item-desc {
      line-height: 0.4rem;
      color: #ccc;
      ellipsis();
    }

    .item-button {
      line-height: 0.44rem;
      margin-top: 0.16rem;
      background: #ff9300;
      padding: 0 0.2rem;
      border-radius: 0.06rem;
      color: #fff;
    }
  }
}
</style>
