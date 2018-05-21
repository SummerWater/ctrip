<template>
  <div>
    <home-header></home-header>
    <home-swiper :swiperList="swiperList"></home-swiper>
    <home-icons :iconList="iconList"></home-icons>
    <home-hot :hotList="hotList" :topIcon="topIcon"></home-hot>
    <home-youlike :itemList="itemList"></home-youlike>
    <home-weekends :weekendList="weekendList"></home-weekends>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeHot from './components/Hot'
import HomeYoulike from './components/Youlike'
import HomeWeekends from './components/Weekends'
import ApiUrl from '@/config/api_url'
import axios from 'axios'

export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeHot,
    HomeYoulike,
    HomeWeekends
  },
  data () {
    return {
      swiperList: [],
      iconList: [],
      hotList: [],
      topIcon: [],
      itemList: [],
      weekendList: []
    }
  },
  methods: {
    getHomeInfo () {
      axios.get(ApiUrl.api + 'index.json')
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      if (res.data.ret && res.data.data) {
        const data = res.data.data
        this.swiperList = data.swiperList
        this.iconList = data.iconList
        this.hotList = data.hotList
        this.topIcon = data.topIcon
        this.itemList = data.itemList
        this.weekendList = data.weekendList
      }
    }
  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>

<style scoped lang="stylus">

</style>
