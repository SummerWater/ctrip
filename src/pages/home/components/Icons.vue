<template>
  <div class="icons">
    <swiper class="icon-wrapper" :options="swiperOption">
      <swiper-slide v-for="(listBlock, key) in list" :key="key">
        <div class="item" v-for="(item,index) in listBlock" :key="index">
          <img :src="item.imgUrl" class="icon-img">
          <p class="icon-title">{{item.title}}</p>
        </div>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
    <div class="location-wrapper border-top">
      <div class="location border-right"><span class="iconfont">&#xe611;</span>定位失败</div>
      <div class="location"><span class="iconfont">&#xe642;</span>5折泡温泉</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      swiperOption: {
        pagination: {
          el: '.swiper-pagination'
        }
      },
      iconList: [
        {
          title: '景点门票',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
        },
        {
          title: '一日游',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png'
        },
        {
          title: '本地玩乐',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/f5/a963333e1fa802.png'
        },
        {
          title: '动植物园',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png'
        },
        {
          title: '必游榜单',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png'
        },
        {
          title: '自然风光',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/96/c70f1e85ae4a4f02.png'
        },
        {
          title: '海滨海岛',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/27/dac2bcf9added702.png'
        },
        {
          title: '踏青赏花',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png'
        },
        {
          title: '城市观光',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png'
        },
        {
          title: '全部玩乐',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/80/416c6ab3368d1f02.png'
        }
      ]
    }
  },
  computed: {
    list () {
      const res = []
      for (let i in this.iconList) {
        const k = Math.floor(i / 8)
        if (!res[k]) {
          res[k] = []
        }
        res[k].push(this.iconList[i])
      }
      return res
    }
  }
}
</script>

<style scoped lang="stylus">
  @import "~styles/variable.styl"
  .icons >>> .swiper-pagination-bullet-active
    background-color $bgColor !important
  .icons
    background-color #fff
  .swiper-slide
    display flex
    flex-wrap wrap
    width 100%
    height 0
    padding-bottom calc(50%)
    overflow hidden
    .item
      overflow hidden
      padding-bottom calc(25% - .4rem)
      width 25%
      height 0
      .icon-img
        display block
        padding .1rem
        width calc(100% - 1.0rem)
        margin 0 auto
        margin-top .05rem
      .icon-title
        text-align center
        line-height .4rem
  .location-wrapper
    display flex
    height 1rem
    line-height 1rem
    .location
      text-align center
      flex 1
</style>
