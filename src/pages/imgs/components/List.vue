<template>
  <div class="list">
    <div class="item" v-for="(item, index) in imgList" :key="index">
      <img :src="item" @click="handleListClick(index)">
    </div>
    <fade>
      <Gallery :currentImg="currentImg" :imgs="imgList" v-show="galleryShow" @close="galleryShow = false"></Gallery>
    </fade>
  </div>
</template>

<script>
import Gallery from '@/common/gallery/Gallery'
import Fade from '@/common/fade/Fade'
export default {
  name: 'ImgsList',
  data () {
    return {
      imgList: [
        'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_350x240_8e61302a.jpg',
        'http://img1.qunarzz.com/sight/p55/201211/04/fbcab3e5d6479ce893835fbb.jpg_350x240_df8ba9f7.jpg',
        'http://img1.qunarzz.com/wugc/p180/201306/16/7f08e81624346b1693835fbb.jpg_350x240_b09a9503.jpg',
        'http://img1.qunarzz.com/wugc/p123/201211/19/a2045d091f02b25493835fbb.png_350x240_cf4cd08e.png',
        'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_350x240_8e61302a.jpg',
        'http://img1.qunarzz.com/sight/p55/201211/04/fbcab3e5d6479ce893835fbb.jpg_350x240_df8ba9f7.jpg',
        'http://img1.qunarzz.com/wugc/p180/201306/16/7f08e81624346b1693835fbb.jpg_350x240_b09a9503.jpg',
        'http://img1.qunarzz.com/wugc/p123/201211/19/a2045d091f02b25493835fbb.png_350x240_cf4cd08e.png',
        'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_350x240_8e61302a.jpg',
        'http://img1.qunarzz.com/sight/p55/201211/04/fbcab3e5d6479ce893835fbb.jpg_350x240_df8ba9f7.jpg',
        'http://img1.qunarzz.com/wugc/p180/201306/16/7f08e81624346b1693835fbb.jpg_350x240_b09a9503.jpg',
        'http://img1.qunarzz.com/wugc/p123/201211/19/a2045d091f02b25493835fbb.png_350x240_cf4cd08e.png',
        'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_350x240_8e61302a.jpg',
        'http://img1.qunarzz.com/sight/p55/201211/04/fbcab3e5d6479ce893835fbb.jpg_350x240_df8ba9f7.jpg',
        'http://img1.qunarzz.com/wugc/p180/201306/16/7f08e81624346b1693835fbb.jpg_350x240_b09a9503.jpg',
        'http://img1.qunarzz.com/wugc/p123/201211/19/a2045d091f02b25493835fbb.png_350x240_cf4cd08e.png'
      ],
      galleryShow: false,
      currentImg: 0
    }
  },
  components: {
    Gallery,
    Fade
  },
  methods: {
    handleListClick: function (index) {
      this.galleryShow = true
      this.currentImg = index
    }
  }
}
</script>

<style scoped lang="stylus">
  .list
    display flex
    flex-wrap wrap
    padding-top .98rem
    .item
      width 50%
      padding 0 .1rem
      margin-bottom .1rem
      box-sizing border-box
      &:nth-child(2n)
        padding-left .05rem
      &:nth-child(2n - 1)
        padding-right .05rem
      img
        width 100%
</style>
