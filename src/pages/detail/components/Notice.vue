<template>
  <div>
    <div class="notice" @click="detailShow = true">
      <span class="iconfont">&#xe657;</span>
      除法定节假日，故宫博物馆实行周一闭馆。
      <span class="iconfont detail">&#xe65e;</span>
    </div>
    <div class="detail-wrapper" v-show="detailShow">
      <div class="content-wrapper">
        <div class="title">
          <span class="iconfont">&#xe657;</span>
          <span>景区公告</span>
        </div>
        <div class="content">除法定节假日，故宫博物馆实行周一闭馆。</div>
        <div class="close" @click="detailShow = false">
          <span class="iconfont">&#xe61a;</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailNotice',
  data () {
    return {
      detailShow: false
    }
  }
}
</script>

<style scoped lang="stylus">
  @import "~styles/mixins.styl"
  .notice
    background-color #fff5e5
    color #ff8300
    padding 0 .2rem
    padding-right .5rem
    line-height .88rem
    position relative
    margin .1rem 0 .2rem 0
    ellipsis()
    .detail
      position absolute
      right .2rem

  .detail-wrapper
    position fixed
    top 0
    left 0
    bottom 0
    right 0
    background-color rgba(255, 255, 255, .85)
    z-index 99
    .content-wrapper
      box-sizing border-box
      min-height 100%
      padding-bottom 1rem
      position relative
      .close
        width 100%
        position absolute
        bottom .3rem
        text-align center
      .title
        text-align center
        padding-top 2rem
        padding-bottom .9rem
        color: #f67353;
        font-size: .4rem;
      .content
        padding 0 .2rem
</style>
