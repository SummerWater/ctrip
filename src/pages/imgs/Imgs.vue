<template>
  <div>
    <imgs-header></imgs-header>
    <imgs-list></imgs-list>
  </div>
</template>

<script>
import ImgsHeader from './components/Header'
import ImgsList from './components/List'
export default {
  name: 'Imgs',
  components: {
    ImgsHeader,
    ImgsList
  }
}
</script>

<style scoped>

</style>
