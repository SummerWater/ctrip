<template>
  <transition>
    <slot></slot>
  </transition>
</template>

<script>
export default {
  name: 'Fade'
}
</script>

<style scoped lang="stylus">
  .v-enter, .v-leave-to
    opacity 0

  .v-enter-active
    transition opacity .5s
</style>
