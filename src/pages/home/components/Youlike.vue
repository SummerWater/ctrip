<template>
  <div class="youlike">
    <div class="like-title">
      <span class="title"><img class="mp-title-img" src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png" alt="猜你喜欢">猜你喜欢</span>
    </div>
    <div class="item border-bottom" v-for="(item, index) in itemList" :key="index">
      <div class="item-img-wrapper">
        <img :src="item.imgUrl" class="item-img">
      </div>
      <div class="item-info">
        <div class="title">{{item.title}}</div>
        <div class="comment">
          <start :num="item.start" class="starts"></start>
          <div class="comment-num">{{item.comment_num}}条评论</div>
        </div>
        <div class="price-wrapper">
          <span class="price">
            <span class="orange">￥{{item.price}}</span>起
          </span>
          <span class="address">{{item.address}}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Start from '@/common/start/Start'
export default {
  name: 'HomeYoulike',
  components: {
    Start
  },
  props: {
    itemList: Array
  }
}
</script>

<style scoped lang="stylus">
  @import "~styles/mixins.styl"
  @import "~styles/variable.styl"
  .youlike
    margin-top .2rem
    background-color #ffffff
    .like-title
      padding .24rem .2rem
      .title
        font-size .32rem
        .mp-title-img
          display inline-block
          vertical-align middle
          margin-bottom .06rem
          margin-right .1rem
          width .30rem
    .item
      display flex
      padding .2rem
      .item-img-wrapper
        width 2rem
        height 2rem
        .item-img
          display block
          width 100%
          height 100%
      .item-info
        flex 1
        padding-right .2rem
        padding-left .2rem
        .title
          font-size .32rem
          padding-top .2rem
          padding-bottom .2rem
        .comment
          display flex
          margin-bottom .4rem
          .comment-num
            padding-top .05rem
            margin-left .2rem
            align-items center
            font-size .24rem
            color #666
        .price-wrapper
          display flex
          justify-content space-between
          .orange
            font-size .36rem
            color $orange
          .address
            font-size .24rem
            color #666
</style>
