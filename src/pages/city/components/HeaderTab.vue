<template>
  <div class="header-tab">
    <span :class="['item', tab === 1 ? 'active' : '']" @click="tab = 1">境内</span>
    <span :class="['item', tab === 2 ? 'active' : '']" @click="tab = 2">境外·港澳台</span>
  </div>
</template>

<script>
export default {
  name: 'CityHeader',
  data () {
    return {
      tab: 1
    }
  }
}
</script>

<style scoped lang="stylus">
  @import "~styles/variable.styl"
  @import "~styles/mixins.styl"
  .header-tab
    background-color $bgColor
    height .80rem
    line-height .80rem
    display flex
    justify-content center
    align-items center
    .item
      color #fff
      border 1px solid #fff
      line-height .4rem
      height .4rem
      width 40%
      text-align center
      &.active
        background-color #ffffff
        color $bgColor
</style>
