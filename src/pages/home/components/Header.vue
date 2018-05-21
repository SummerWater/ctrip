<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont back-icon">&#xe624;</span>
    </div>
    <div class="header-search">
      <span class="iconfont search-icon">&#xe632;</span>
      <span class="search-title">输入城市/景点/游玩主题</span>
    </div>
    <router-link to="/city">
      <div class="header-right">
        <span class="city-name">{{city}}</span>
        <span class="iconfont arrow-bottom">&#xe64a;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
import {mapState} from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>

<style scoped lang="stylus">
  @import "~styles/variable.styl"
  .header
    display flex
    height $topHeight
    line-height $topHeight
    overflow hidden
    background-color $bgColor
    color #fff
    .header-left
      width .88rem
      text-align center
      .back-icon
        font-size .34rem
        font-weight bold
    .header-search
      flex 1
      width 100%
      height .6rem
      line-height .6rem
      margin-top .12rem
      font-size .28rem
      box-sizing border-box
      padding-left .2rem
      border-radius .04rem
      background-color #fff
      color #ddd
    .header-right
      color #fff
      padding 0 .2rem
      .arrow-bottom
        font-size .26rem
</style>
