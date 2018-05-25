<template>
  <div class="recommend">
    <div class="title border-bottom"><span class="iconfont good">&#xe650;</span>去哪儿推荐</div>
    <div class="recommend-list">
      <div class="item border-bottom" v-for="recommend in recommendList" :key="recommend.id">
        <div class="info">
          <div class="title">{{recommend.title}}</div>
          <div class="tips"><span class="iconfont">&#xe608;</span>{{recommend.timeLimit}}</div>
          <div class="tags">
            <span v-for="(tag,index) in recommend.tags" :key="index">{{tag}}</span>
          </div>
        </div>
        <div class="price-wrapper">
          <div class="v-center">
            <div class="price">￥{{recommend.price}}</div>
            <button class="reserve-btn">预定</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailRecommend',
  data () {
    return {
      recommendList: [
        {
          id: '1',
          title: '【当日票】故宫成人票凭身份证入园（随买随用，快速入园）',
          timeLimit: '15:45前随买随用',
          tags: ['自营', '无需换票', '条件退'],
          price: '60'
        },
        {
          id: '2',
          title: '【上午场】故宫成人票+故宫全景手绘地图',
          timeLimit: '23:59前可订明日',
          tags: ['自营', '不可退'],
          price: '70.0'
        },
        {
          id: '3',
          title: '【去哪儿专线】天安门+故宫+八达岭+鸟巢（配耳麦+赠珍宝馆）',
          timeLimit: '可订明日',
          tags: ['条件退', '无购物', '已售2753'],
          price: '158.0'
        }
      ]
    }
  }
}
</script>

<style scoped lang="stylus">
  @import "~styles/variable.styl"
  .recommend
    background-color #fff
    .title
      line-height .88rem
      padding 0 .2rem
      font-size .30rem
      .good
        background: rgba(255, 0, 0, 0.41);
        color: #fff;
        font-size .24rem
        width: .4rem;
        height: .4rem;
        line-height: .4rem;
        border-radius: .4rem;
        display: inline-block;
        vertical-align middle
        margin-bottom .06rem
        text-align: center;
        margin-right .2rem
    .recommend-list
      .item
        display flex
        padding .2rem 0
        .info
          width 75%
          .title
            line-height .5rem
            max-height 1rem
            overflow hidden
            color #555
          .tips
            color #666
            font-size .24rem
            padding 0 .2rem
            margin .2rem 0
            .iconfont
              font-size .24rem
              color #00d7ed
          .tags
            display flex
            span
              color #00afc7
              font-size .24rem
              margin-left .2rem
        .price-wrapper
          width 25%
          display flex
          align-items center
          .v-center
            width 100%
          .price
            color $orange
            text-align center
            font-size .32rem
            font-weight bold
          .reserve-btn
            background linear-gradient(130deg,#ffab1e 37%,#ff8c12 100%)
            width 80%
            display block
            margin 0 auto
            color: #fff;
            line-height: .6rem;
            border-radius: .1rem;
</style>
