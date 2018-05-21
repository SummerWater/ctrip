<template>
  <div class="header">
    <router-link to="/">
      <span class="iconfont detail-back" v-show="showAbs">&#xe624;</span>
    </router-link>
    <div class="detail-header" v-show="!showAbs" :style="styleOptions">
      <router-link to="/">
        <span class="iconfont back">&#xe624;</span>
      </router-link>
      <span class="title">故宫</span>
    </div>
    <div class="img-wrapper">
      <router-link to="/imgs">
        <img src="//img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_600x330_f922b488.jpg" class="detail-img">
      </router-link>
    </div>
    <div class="detail-info">
      <div class="img-number"><span class="iconfont">&#xe626;</span>10</div>
      <div class="info">故宫(AAAAA景区)</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailHeader',
  data () {
    return {
      showAbs: true,
      styleOptions: {
        opacity: 0
      }
    }
  },
  methods: {
    scrollHeader () {
      const top = document.body.scrollTop
      if (top > 0) {
        let t = top / 100
        if (t > 1) {
          t = 1
        }
        this.styleOptions.opacity = t
        this.showAbs = false
      } else {
        this.showAbs = true
      }
    }
  },
  mounted () {
    document.addEventListener('scroll', this.scrollHeader)
  },
  beforeDestroy () {
    document.removeEventListener('scroll', this.scrollHeader)
  }
}
</script>

<style scoped lang="stylus">
  @import "~styles/variable.styl"
  .header
    width 100%
    height 0
    padding-bottom 55%
    position relative
    overflow hidden
    .detail-img
      width 100%
    .detail-back
      position absolute
      left .1rem
      top .1rem
      width .72rem
      height .72rem
      line-height .72rem
      border-radius .36rem
      text-align center
      color #fff
      font-weight bold
      font-size .36rem
      background-color rgba(0,0,0,0.5)
    .detail-info
      position absolute
      width 100%
      left 0
      bottom 0
      padding-left .2rem
      &:after
        content: ' '
        position absolute
        left 0
        bottom 0
        width 100%
        height .6rem
        line-height .6rem
        background: linear-gradient(top, transparent, #000);
        z-index 1
      .img-number
        display inline-block
        padding 0 .26rem
        border-radius .1rem
        line-height .36rem
        color #fff
        background-color rgba(0,0,0,.6)
      .info
        position relative
        font-size .36rem
        line-height .9rem
        height .9rem
        color #fff
        z-index 2
    .detail-header
      position fixed
      z-index 99
      top 0
      left 0
      background-color $bgColor
      width 100%
      height $topHeight
      line-height $topHeight
      text-align center
      .title
        color #fff
        font-size .36rem
      .back
        position absolute
        left 0
        width .88rem
        color #ffffff
        font-size 0.34rem
        font-weight bold
        text-align center
</style>
