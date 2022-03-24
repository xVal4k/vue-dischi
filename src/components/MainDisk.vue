<template>
<main>
  <div v-if="arrDisks == null">Just a moment</div>
  <div v-else class="row row_disk">
    <card-disk v-for="disk in arrDisks" :key="disk.id" :diskData="disk"/>
  </div>
</main>
</template>

<script>
/* eslint-disable */

import CardDisk from './CardDisk.vue'
import axios from 'axios'

export default {
  name: 'MainDisk',
  components: {
    CardDisk
  },
  data () {
    return {
      APIurl: 'https://flynn.boolean.careers/exercises/api/array/music',
      arrDisks: null
    }
  },
  created () {
    axios
      .get(this.APIurl)
      .then((response) => {
        this.arrDisks = response.data.response.map((disk) => ({
          title: disk.title,
          poster: disk.poster,
          author: disk.author,
          year: disk.year
        }))
      })
  }
}
</script>

<style lang="scss" scoped>
  main {
    background-color: #1E2D3B;

    .row_disk {
      width: 70%;
      margin: 0 auto;
      padding: 3rem 0;
    }
  }
</style>
