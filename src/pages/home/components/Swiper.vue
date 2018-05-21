<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(item,index) in swiperList" :key="index">
        <img :src="item" class="swiper-item">
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    swiperList: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: {
          el: '.swiper-pagination'
        },
        autoplay: true
      }
    }
  }
}
</script>

<style scoped lang="stylus">
  .wrapper >>> .swiper-pagination-bullet-active
    background-color #fff !important
  .wrapper
    overflow hidden
    background-color #ddd
    height 0
    width 100%
    padding-bottom 26.7%
  .swiper-item
    width 100%
</style>
