<template>
  <div class="header">
    <router-link to="/">
      <span class="iconfont city-back">&#xe624;</span>
    </router-link>
    <span class="title">城市选择</span>
  </div>
</template>

<script>
export default {
  name: 'CityHeaderTab'
}
</script>

<style scoped lang="stylus">
  @import "~styles/variable.styl"
  @import "~styles/mixins.styl"
  .header
    background-color $bgColor
    height $topHeight
    line-height $topHeight
    text-align center
    position relative
    .title
      color #fff
      font-size .32rem
    .city-back
      position absolute
      width .88rem
      left 0
      top 0
      color #fff
      font-size .34rem
      font-weight bold
</style>
