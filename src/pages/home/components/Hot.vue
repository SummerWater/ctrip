<template>
  <div class="hot">
    <div class="hot-title">
      <span class="title"><img class="mp-title-img" src="http://img1.qunarzz.com/piao/fusion/1711/16/bfbb9874e8f11402.png" alt="本周热门榜单">本周热门榜单</span>
      <span class="more">全部榜单></span>
    </div>
    <ul class="hot-wrapper">
      <router-link tag="li" :to="'/detail/' + index" class="hot-item" v-for="(item, index) in hotList" :key="index" :ref="'hot_' + index">
      <span class="top" v-if="index >= 0 && index < 3">
        <img :src="topIcon[index]" class="top-img" />
      </span>
        <img :src="item.imgUrl" class="hot-img">
        <p class="title">{{item.title}}</p>
        <p class="price">
          <span class="orange">{{item.price}}</span>起
        </p>
      </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeHot',
  props: {
    hotList: Array,
    topIcon: Array
  }
}
</script>

<style scoped lang="stylus">
  @import "~styles/mixins.styl"
  .hot
    margin-top .2rem
    background-color #ffffff
    .hot-title
      padding .24rem .2rem
      .title
        font-size .32rem
        .mp-title-img
          display inline-block
          vertical-align middle
          margin-bottom .06rem
          margin-right .1rem
          width .30rem
      .more
        font-size .26rem
        color #666
        line-height .4rem
        float right
    .hot-wrapper
      display flex
      padding .2rem 0
      overflow-x scroll
      overflow-y hidden
      .hot-item
        margin-left .2rem
        width 2rem
        position relative
        .top
          position absolute
          left -.05rem
          top -.05rem
          width .84rem
          height .4rem
          .top-img
            width 100%
        .hot-img
          width 2rem
          height 2rem
        .title
          ellipsis()
          font-size .24rem
          padding-top .1rem
          padding-bottom .1rem
          text-align center
        .price
          font-size .24rem
          text-align center
          .orange
            font-size .28rem
            color #ff8300
</style>
