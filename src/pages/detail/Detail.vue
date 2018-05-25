<template>
  <div>
    <detail-header></detail-header>
    <detail-base-info></detail-base-info>
    <detail-notice></detail-notice>
    <detail-recommend></detail-recommend>
    <div class="content"></div>
  </div>
</template>

<script>
import DetailHeader from './components/Header'
import DetailBaseInfo from './components/BaseInfo'
import DetailNotice from './components/Notice'
import DetailRecommend from './components/Recommend'

export default {
  name: 'Detail',
  components: {
    DetailHeader,
    DetailBaseInfo,
    DetailNotice,
    DetailRecommend
  }
}
</script>

<style scoped>
  .content {
    height: 15rem;
  }
</style>
