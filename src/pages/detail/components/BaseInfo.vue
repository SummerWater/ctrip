<template>
  <div class="detail-base-info">
    <div class="base-info">
      <div class="info-wrapper border-right">
        <div class="number"><span class="showy">5.0</span>分 超赞</div>
        <div class="comment-num">222653条评论 85条攻略</div>
        <span class="iconfont">&#xe65e;</span>
      </div>
      <div class="address-wrapper">
        <div class="brief">景点简介</div>
        <div class="tips">开放时间、贴士</div>
        <span class="iconfont">&#xe65e;</span>
      </div>
    </div>
    <div class="addres-info">
      <span class="iconfont addr">&#xe64e;</span>
      <span class="title">北京市东城区景山前街4号</span>
      <span class="iconfont detail">&#xe65e;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailBaseInfo'
}
</script>

<style scoped lang="stylus">
  @import "~styles/variable.styl"
  .detail-base-info
    .base-info
      position relative
      z-index 1
      top -.1rem
      background-color #fff
      border-radius .1rem .1rem 0 0
      display flex
      padding .2rem 0
      .info-wrapper
        width 50%
        padding 0 .2rem
        position relative
        .number
          color $orange
          margin-bottom .1rem
          line-height .40rem
          height .40rem
          display inline-block
          .showy
            font-size .44rem
        .comment-num
          color #999
          font-size .24rem
        .iconfont
          position absolute
          right .2rem
          top 50%
          transform translate(0, -50%)
          color #999
      .address-wrapper
        width 50%
        padding 0 .2rem
        position relative
        .brief
          color #333
          margin-bottom .1rem
          line-height .40rem
          height .40rem
          display inline-block
        .tips
          color #999
          font-size .24rem
        .iconfont
          position absolute
          right .2rem
          top 50%
          transform translate(0, -50%)
          color #999
    .addres-info
      position relative
      top -.1rem
      padding .26rem .2rem
      background-color #fff
      .addr
        margin-right .1rem
      .detail
        position absolute
        right .2rem
</style>
