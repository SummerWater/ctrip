<template>
  <div>
    <detail-header></detail-header>
    <detail-base-info></detail-base-info>
    <detail-notice></detail-notice>
    <div class="content"></div>
  </div>
</template>

<script>
import DetailHeader from './components/Header'
import DetailBaseInfo from './components/BaseInfo'
import DetailNotice from './components/Notice'

export default {
  name: 'Detail',
  components: {
    DetailHeader,
    DetailBaseInfo,
    DetailNotice
  }
}
</script>

<style scoped>
  .content {
    height: 15rem;
  }
</style>
