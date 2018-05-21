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
      }
    }
  },
  props: {
    iconList: Array
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
