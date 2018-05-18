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
  data () {
    return {
      swiperOption: {
        loop: true,
        pagination: {
          el: '.swiper-pagination'
        },
        autoplay: true
      },
      swiperList: [
        'http://img1.qunarzz.com/piao/fusion/1805/77/f63bd04dd5319602.jpg_750x200_6ba8e0ca.jpg',
        'http://img1.qunarzz.com/piao/fusion/1804/c4/1cdd28811593b802.jpg_750x200_5fbb7c91.jpg',
        'http://img1.qunarzz.com/piao/fusion/1804/84/6334efc67b637902.jpg_750x200_598f99fc.jpg',
        'http://img1.qunarzz.com/piao/fusion/1804/e5/82b53c47166cfc02.jpg_750x200_0d3a0066.jpg',
        'http://img1.qunarzz.com/piao/fusion/1804/b7/c500761d01694702.jpg_750x200_a2922234.jpg',
        'http://img1.qunarzz.com/piao/fusion/1804/b7/c500761d01694702.jpg_750x200_a2922234.jpg'
      ]
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
