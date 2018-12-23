<template>
  <div class="icons">
    <swiper>
      <!-- slides -->
      <swiper-slide v-for="( page,index ) of pages"
                    :key="index" >
      <div class="icon"
           v-for="item in page"
           :key="item.id">
        <div class="icon-img">
          <img class="icon-img-content"
               :src="item.imgUrl" />
        </div>
        <p class="icon-desc" >{{ item.desc }}</p>
      </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  data () {
    return {
      list: [
        {
          id: '0001',
          imgUrl: 'https://s.qunarzz.com/homestatic/app/qunar.png',
          desc: '景点门票景点门票景点门票景点门票景点门票'
        }, {
          id: '0002',
          imgUrl: 'https://s.qunarzz.com/homestatic/app/qunar.png',
          desc: '滑雪季'
        }, {
          id: '0003',
          imgUrl: 'https://s.qunarzz.com/homestatic/app/qunar.png',
          desc: '泡温泉'
        }, {
          id: '0004',
          imgUrl: 'https://s.qunarzz.com/homestatic/app/qunar.png',
          desc: '动植物园'
        }, {
          id: '0005',
          imgUrl: 'https://s.qunarzz.com/homestatic/app/qunar.png',
          desc: '动植物园'

        }, {
          id: '0006',
          imgUrl: 'https://s.qunarzz.com/homestatic/app/qunar.png',
          desc: '动植物园'

        }, {
          id: '0007',
          imgUrl: 'https://s.qunarzz.com/homestatic/app/qunar.png',
          desc: '动植物园'

        }, {
          id: '0008',
          imgUrl: 'https://s.qunarzz.com/homestatic/app/qunar.png',
          desc: '动植物园'
        }, {
          id: '0009',
          imgUrl: 'https://s.qunarzz.com/homestatic/app/qunar.png',
          desc: '动植物园'
        }
      ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.list.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';

.icons >>> .swiper-container {
  height: 0;
  padding-bottom: 50%;
  .icons{
   margin-top: .1rem
  }
  .icon {
    position: relative;
    overflow: hidden;
    width: 25%;
    float: left;
    padding-bottom: 25%;
    height: 0;

    .icon-img {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0.44rem;
      padding: 0.1rem;
      box-sizing: border-box;

      .icon-img-content {
        height: 100%;
        display: block;
        margin: 0 auto;
      }
    }

    .icon-desc {
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      height: 0.44rem;
      line-height: 0.44rem;
      color: $darkTextcolor;
      text-align: center;
      overflow: hidden;
      white-space: nowrap;
      text-overflow :ellipsis;
    }
  }
}

</style>
