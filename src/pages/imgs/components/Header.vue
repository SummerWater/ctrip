<template>
  <div class="header">
    <router-link to="/detail/1">
      <span class="iconfont city-back">&#xe624;</span>
    </router-link>
    <span class="title">景区图片</span>
  </div>
</template>

<script>
export default {
  name: 'ImgsHeader'
}
</script>

<style scoped lang="stylus">
  @import "~styles/variable.styl"
  @import "~styles/mixins.styl"
  .header
    position fixed
    top 0
    left 0
    width 100%
    background-color #fff
    height $topHeight
    line-height $topHeight
    text-align center
    border-bottom 1px solid #ddd
    .title
      color #333
      font-size .32rem
    .city-back
      position absolute
      width .88rem
      left 0
      top 0
      color #333
      font-size .34rem
      font-weight bold
</style>
