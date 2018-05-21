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
  data () {
    return {
      itemList: [
        {
          title: '大连森林动物园',
          start: 4,
          comment_num: 11175,
          price: 58,
          address: '西岗区',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1707/57/5729585581b6732fa3.water.jpg_200x200_85298361.jpg'
        },
        {
          title: '大连圣亚海洋世界',
          start: 5,
          comment_num: 20645,
          price: 25,
          address: '沙河口区',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_200x200_4ab5da75.jpg'
        },
        {
          title: '海昌发现王国',
          start: 5,
          comment_num: 15362,
          price: 60,
          address: '金石滩旅...',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1703/94/944fc059260bd728a3.water.jpg_200x200_742cb84f.jpg'
        },
        {
          title: '大连森林动物园',
          start: 4,
          comment_num: 11175,
          price: 58,
          address: '西岗区',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1707/57/5729585581b6732fa3.water.jpg_200x200_85298361.jpg'
        },
        {
          title: '大连圣亚海洋世界',
          start: 5,
          comment_num: 20645,
          price: 25,
          address: '沙河口区',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_200x200_4ab5da75.jpg'
        },
        {
          title: '海昌发现王国',
          start: 5,
          comment_num: 15362,
          price: 60,
          address: '金石滩旅...',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1703/94/944fc059260bd728a3.water.jpg_200x200_742cb84f.jpg'
        },
        {
          title: '大连森林动物园',
          start: 4,
          comment_num: 11175,
          price: 58,
          address: '西岗区',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1707/57/5729585581b6732fa3.water.jpg_200x200_85298361.jpg'
        },
        {
          title: '大连圣亚海洋世界',
          start: 5,
          comment_num: 20645,
          price: 25,
          address: '沙河口区',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_200x200_4ab5da75.jpg'
        },
        {
          title: '海昌发现王国',
          start: 5,
          comment_num: 15362,
          price: 60,
          address: '金石滩旅...',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1703/94/944fc059260bd728a3.water.jpg_200x200_742cb84f.jpg'
        },
        {
          title: '大连森林动物园',
          start: 4,
          comment_num: 11175,
          price: 58,
          address: '西岗区',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1707/57/5729585581b6732fa3.water.jpg_200x200_85298361.jpg'
        },
        {
          title: '大连圣亚海洋世界',
          start: 5,
          comment_num: 20645,
          price: 25,
          address: '沙河口区',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_200x200_4ab5da75.jpg'
        },
        {
          title: '海昌发现王国',
          start: 5,
          comment_num: 15362,
          price: 60,
          address: '金石滩旅...',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1703/94/944fc059260bd728a3.water.jpg_200x200_742cb84f.jpg'
        }
      ]
    }
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
