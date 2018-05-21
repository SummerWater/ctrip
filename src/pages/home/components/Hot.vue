<template>
  <div class="hot">
    <div class="hot-title">
      <span class="title"><img class="mp-title-img" src="http://img1.qunarzz.com/piao/fusion/1711/16/bfbb9874e8f11402.png" alt="本周热门榜单">本周热门榜单</span>
      <span class="more">全部榜单></span>
    </div>
    <ul class="hot-wrapper">
      <li class="hot-item" v-for="(item, index) in hotList" :key="index" :ref="'hot_' + index">
        <span class="top" v-if="index >= 0 && index < 3">
          <img :src="topIcon[index]" class="top-img" />
        </span>
        <img :src="item.imgUrl" class="hot-img">
        <p class="title">{{item.title}}</p>
        <p class="price">
          <span class="orange">{{item.price}}</span>起
        </p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeHot',
  data () {
    return {
      hotList: [
        {
          title: '大连森林动物园',
          price: '￥58',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1707/57/5729585581b6732fa3.water.jpg_150x150_88ed4437.jpg'
        },
        {
          title: '大连圣亚海洋世界',
          price: '￥25',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_150x150_2c4b6f2f.jpg'
        },
        {
          title: '老虎滩海洋公园',
          price: '￥50',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1602/39/39f6b1003abe1b2790.img.jpg_150x150_a9877501.jpg'
        },
        {
          title: '旅顺203樱花园',
          price: '￥218',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1804/a2/a2a3dd4f0bf42f4da3.img.jpg_150x150_e9128a33.jpg'
        },
        {
          title: '海昌发现王国',
          price: '￥60',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1703/94/944fc059260bd728a3.water.jpg_150x150_f3152ca6.jpg'
        },
        {
          title: '大连森林动物园',
          price: '￥58',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1707/57/5729585581b6732fa3.water.jpg_150x150_88ed4437.jpg'
        },
        {
          title: '大连圣亚海洋世界',
          price: '￥25',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_150x150_2c4b6f2f.jpg'
        },
        {
          title: '老虎滩海洋公园',
          price: '￥50',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1602/39/39f6b1003abe1b2790.img.jpg_150x150_a9877501.jpg'
        },
        {
          title: '旅顺203樱花园',
          price: '￥218',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1804/a2/a2a3dd4f0bf42f4da3.img.jpg_150x150_e9128a33.jpg'
        },
        {
          title: '海昌发现王国',
          price: '￥60',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1703/94/944fc059260bd728a3.water.jpg_150x150_f3152ca6.jpg'
        }
      ],
      topIcon: [
        'http://img1.qunarzz.com/piao/fusion/1710/ab/159673b63e6ca702.png',
        'http://img1.qunarzz.com/piao/fusion/1710/2d/36d0c4adaebbbc02.png',
        'http://img1.qunarzz.com/piao/fusion/1710/67/edc47ffef9e96b02.png'
      ]
    }
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
