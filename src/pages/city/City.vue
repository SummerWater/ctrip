<template>
  <div>
    <city-header></city-header>
    <city-header-tab></city-header-tab>
    <city-list :hotCities="hotCities" :cities="cities"></city-list>
  </div>
</template>

<script>
import CityHeader from './components/Header'
import CityHeaderTab from './components/HeaderTab'
import CityList from './components/List'
import ApiUrl from '@/config/api_url'
import axios from 'axios'

export default {
  name: 'City',
  data () {
    return {
      hotCities: [],
      cities: []
    }
  },
  components: {
    CityHeader,
    CityHeaderTab,
    CityList
  },
  methods: {
    getCityInfo () {
      axios.get(ApiUrl.api + '/city.json')
        .then(this.getCityInfoSucc)
    },
    getCityInfoSucc (res) {
      if (res.data.ret && res.data) {
        const data = res.data.data
        this.hotCities = data.hotCities
        this.cities = data.cities
      }
    }
  },
  mounted () {
    this.getCityInfo()
  }
}
</script>

<style scoped>

</style>
