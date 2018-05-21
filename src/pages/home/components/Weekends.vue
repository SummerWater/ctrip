<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of weekendList" :key="item.id">
        <img :src="item.imgUrl" class="item-img"/>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekends',
  props: {
    weekendList: Array
  }
}
</script>

<style scoped lang="stylus">
  @import "~styles/mixins.styl"
  .title
    line-height .8rem
    text-indent .2rem
    background-color #eee
  .item
    overflow hidden
    .item-img
      width 100%
    .item-info
      padding .3rem .2rem
      .item-title
        line-height .4rem
        font-size .3rem
        ellipsis()
      .item-desc
        line-height .4rem
        font-size .2rem
        color #666
        ellipsis()
      .item-button
        margin-top .16rem
        padding 0 .2rem
        border-radius .06rem
        color #fff
        background-color #ff9300
</style>
