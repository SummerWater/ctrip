<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-hot></home-hot>
    <home-youlike></home-youlike>
    <home-weekends></home-weekends>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeHot from './components/Hot'
import HomeYoulike from './components/Youlike'
import HomeWeekends from './components/Weekends'

export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeHot,
    HomeYoulike,
    HomeWeekends
  }
}
</script>

<style scoped lang="stylus">

</style>
