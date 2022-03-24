<template>
  <div id="app">
    <header-disk />
    <main-disk />
  </div>
</template>

<script>
/* eslint-disable */

import HeaderDisk from './components/HeaderDisk.vue'
import MainDisk from './components/MainDisk.vue'

export default {
  name: 'App',
  components: {
    HeaderDisk,
    MainDisk
  }
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap";
</style>
