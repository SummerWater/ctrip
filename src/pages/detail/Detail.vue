<template>
  <div>
    <detail-header></detail-header>
    <detail-base-info></detail-base-info>
    <div class="content"></div>
  </div>
</template>

<script>
import DetailHeader from './components/Header'
import DetailBaseInfo from './components/BaseInfo'
export default {
  name: 'Detail',
  components: {
    DetailHeader,
    DetailBaseInfo
  }
}
</script>

<style scoped>
  .content {
    height: 15rem;
  }
</style>
