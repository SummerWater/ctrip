<template>
  <div>
    <city-header></city-header>
    <city-header-tab></city-header-tab>
  </div>
</template>

<script>
import CityHeader from './components/Header'
import CityHeaderTab from './components/HeaderTab'
export default {
  name: 'City',
  components: {
    CityHeader,
    CityHeaderTab
  }
}
</script>

<style scoped>

</style>
