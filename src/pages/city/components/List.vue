<template>
  <div class="list">
    <div class="list-item">
      <div class="title">热门城市</div>
      <div class="item-wrapper">
        <div class="item" v-for="item in hotCities" :key="item.id" @click="handleCityChange(item.name)">{{item.name}}</div>
      </div>
    </div>
    <div class="list-item alphabet">
      <div class="title">字母排序</div>
      <div class="item-wrapper">
        <div class="item" v-for="item in alphabet" :key="item" @click="alphaIndex(item)">{{item}}</div>
      </div>
    </div>
    <div class="list-item city" v-for="(item, index) in cities" :key="index" :ref="'alpha-' + index">
      <div class="title">{{index}}</div>
      <div class="item-wrapper">
        <div class="item" v-for="city in item" :key="city.id" @click="handleCityChange(city.name)">{{city.name}}</div>
        <div class="bt"></div>
      </div>
    </div>
  </div>
</template>

<script>
import {mapMutations} from 'vuex'
export default {
  name: 'CityList',
  props: {
    hotCities: Array,
    cities: [Object, Array]
  },
  computed: {
    alphabet () {
      const res = []
      for (let k in this.cities) {
        res.push(k)
      }
      return res
    }
  },
  methods: {
    alphaIndex (index) {
      const dom = this.$refs['alpha-' + index][0]
      const top = dom.offsetTop
      document.body.scrollTop = top
    },
    handleCityChange (name) {
      this.changeCity(name)
      this.$router.push('/')
    },
    ...mapMutations(['changeCity'])
  }
}
</script>

<style scoped lang="stylus">
  @import "~styles/mixins.styl"
  .list
    .list-item
      .title
        font-size .24rem
        padding-left .2rem
        line-height .72rem
        height .72rem
      .item-wrapper
        display flex
        flex-wrap wrap
        justify-content space-between
        .item
          height .9rem
          line-height .9rem
          text-align center
          width calc(100% / 3 - .01rem)
          margin-bottom .02rem
          background-color #fff
      &.alphabet
        .item-wrapper
          padding .3rem 0
          justify-content flex-start
          background-color #fff
          .item
            margin 0
            width calc(100% / 6)
      &.city
        .item-wrapper
          justify-content flex-start
          background-color #fff
          position relative
          .bt
            position absolute
            width 100%
            height .04rem
            background-color #fff
            bottom 0
            left 0
            z-index 1
          .item
            border-bottom .02rem solid #ddd
            box-sizing border-box
            width 25%
            padding 0 .1rem
            ellipsis()
</style>
