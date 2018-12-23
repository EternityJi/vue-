<template>
  <div class="wraper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide><img class="Swiperimg"
             src="//img1.qunarzz.com/vc/f5/10/9c/b647d3ee724a720ce0fa6101f0.jpg"></swiper-slide>
      <swiper-slide><img class="Swiperimg"
             src="//img1.qunarzz.com/vc/30/e6/6c/7236d07f50947d523bcdeadae8.jpg"></swiper-slide>
      <swiper-slide><img src=""></swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"
           slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination'
      }
    }
  }
}
</script>
<style lang="stylus" scoped>
.wraper >>> .swiper-pagination-bullet-active {
  background-color: red !important;
}
.Swiperimg {
  width: 100%;
  height: 200px;
}

.wraper {
  overflow: hidden;
  background: gray;
}
</style>
