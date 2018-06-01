<template>
  <div>
    <detail-header></detail-header>
    <detail-base-info></detail-base-info>
    <detail-notice></detail-notice>
    <detail-recommend></detail-recommend>
    <detail-ticket-nav></detail-ticket-nav>
    <div class="content"></div>
  </div>
</template>

<script>
import DetailHeader from './components/Header'
import DetailBaseInfo from './components/BaseInfo'
import DetailNotice from './components/Notice'
import DetailRecommend from './components/Recommend'
import DetailTicketNav from './components/TicketNav'

export default {
  name: 'Detail',
  components: {
    DetailHeader,
    DetailBaseInfo,
    DetailNotice,
    DetailRecommend,
    DetailTicketNav
  }
}
</script>

<style scoped>
  .content {
    height: 15rem;
  }
</style>
