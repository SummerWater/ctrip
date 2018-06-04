<template>
  <div class="ticket">
    <div v-for="ticket in tickets" :key="ticket.id">
      <div class="main-title border-bottom">
        <span class="iconfont">&#xe659;</span>
        <span class="title">{{ticket.title}}</span>
      </div>
      <div class="ticket-wrapper">
        <div class="ticket-item border-bottom" v-for="detail in ticket.data" :key="detail.id">
          <div class="ticket-item-title">
            <div class="ticket-info">
              <div class="title">{{detail.title}}</div>
              <div class="desc">{{detail.desc}}</div>
            </div>
            <div class="ticket-price">
            <span class="orange">
              ￥<span class="price">{{detail.price}}</span>
            </span>
              <span class="gray">起</span>
              <span class="iconfont">&#xe65e;</span>
            </div>
          </div>
          <div class="ticket-detail-wrapper">
            <div class="detail-item recommend-list">
              <div class="item border-bottom" v-for="d in detail.detail" :key="d.id">
                <div class="info">
                  <div class="title">{{d.title}}</div>
                  <div class="tips"><span class="iconfont">&#xe608;</span>{{d.time}}</div>
                  <div class="tags">
                    <span v-for="(tag, index) in d.tags" :key="index">{{tag}}</span>
                  </div>
                  <div class="supplier">
                    {{d.supplier}} | 预定须知 <span class="iconfont">&#xe65e;</span>
                  </div>
                </div>
                <div class="price-wrapper">
                  <div class="v-center">
                    <div class="price">￥{{d.price}}</div>
                    <button class="reserve-btn">预定</button>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailTicket',
  data () {
    return {
      tickets: [
        {
          'id': 1,
          'title': '故宫预售成人票',
          'data': [
            {
              'id': 1,
              'title': '上午场',
              'desc': '凭身份证入园',
              'price': 60,
              'detail': [
                {
                  'id': 1,
                  'title': '【上午场】故宫成人票凭身份证入园（快速入园）',
                  'time': '23:59前可订明日',
                  'tags': ['自营', '无需换票', '条件退'],
                  'supplier': '爱上旅行网',
                  'price': 60
                }
              ]
            },
            {
              'id': 2,
              'title': '下午场',
              'desc': '凭身份证入园',
              'price': 60,
              'detail': [
                {
                  'id': 1,
                  'title': '【下午场】故宫成人票凭身份证入园（快速入园）',
                  'time': '23:59前可订明日',
                  'tags': ['自营', '无需换票', '条件退'],
                  'supplier': '爱上旅行网',
                  'price': 60
                },
                {
                  'id': 2,
                  'title': '【下午场】故宫成人票凭身份证入园（快速入园）',
                  'time': '23:59前可订明日',
                  'tags': ['自营', '无需换票', '条件退'],
                  'supplier': '爱上旅行网',
                  'price': 60
                }
              ]
            }
          ]
        }
      ]
    }
  }
}
</script>

<style scoped lang="stylus">
  @import "~styles/variable.styl"
  .ticket
    background-color #ffffff
    .main-title
      line-height .8rem
      padding 0 .2rem
      font-size .32rem
      .iconfont
        color $bgColor
        font-size .36rem
    .ticket-wrapper
      .ticket-item-title
        display flex
        justify-content space-between
        padding 0 .2rem
        line-height .8rem
        .ticket-info
          display flex
          .title
            color #333
          .desc
            color #999
            font-size .24rem
            margin-left .2rem
      .ticket-price
        .orange
          color $orange
          .price
            font-size .40rem
        .gray
          color #999
          font-size .24rem
        .iconfont
          color #999
      .ticket-detail-wrapper
        background-color #f5f5f5
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
                padding-left .2rem
              .tips
                color #666
                font-size .24rem
                padding 0 .2rem
                margin .2rem 0
                .iconfont
                  font-size .24rem
                  color $bgColor
                  margin-right .1rem
              .tags
                display flex
                span
                  color #00afc7
                  font-size .24rem
                  margin-left .2rem
                  margin-bottom .1rem
              .supplier
                font-size .24rem
                padding 0 .2rem
                color #666
                .iconfont
                  font-size .20rem
                  color #666
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
