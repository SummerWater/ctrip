<template>
  <div class="ticket-nav border-bottom">
    <div
      :class="['item', currentNav === index ? 'active' : '']" v-for="(nav, index) in ticketNav" :key="index" @click="handleTicketNavClick(index)">{{nav}}</div>
  </div>
</template>

<script>
export default {
  name: 'DetailTicketNav',
  data () {
    return {
      ticketNav: ['门票', '一日游', '热销组合', '景区服务'],
      currentNav: 0
    }
  },
  methods: {
    handleTicketNavClick (index) {
      this.currentNav = index
    }
  }
}
</script>

<style scoped lang="stylus">
  @import "~styles/variable.styl"
  .ticket-nav
    margin-top .2rem
    line-height 1rem
    height 1rem
    display flex
    background #fff
    .item
      width 25%
      text-align center
      line-height 1rem
      &.active
        border-bottom 2px solid $bgColor
</style>
