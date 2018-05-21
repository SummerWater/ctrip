<template>
  <div>
    <detail-header></detail-header>
    <div class="content"></div>
  </div>
</template>

<script>
import DetailHeader from './components/Header'
export default {
  name: 'Detail',
  components: {
    DetailHeader
  }
}
</script>

<style scoped>
  .content {
    height: 15rem;
  }
</style>
