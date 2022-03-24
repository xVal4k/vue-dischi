<template>
  <div class="container-fluid p-3 text-center col_disk">
    <img :src="diskData.poster" :alt="diskData.title">
    <h3>{{ diskData.title }}</h3>
    <p>{{ diskData.author }}</p>
    <p>{{ diskData.year }}</p>
  </div>
</template>

<script>
/* eslint-disable */

export default {
  name: 'CardDisk',
  props: {
    diskData: Object
  }
}
</script>

<style lang="scss" scoped>
  .col_disk {
    width: calc((100% / 5) - 2rem);
    background: #2E3A46;
    margin: .5rem 1rem;

    img {
      width: 100%;
    }

    h3 {
      line-height: 1.5rem;
      color: white;
      margin: 1rem 0;
    }

    p {
      color: grey;
      margin: 0;
    }
  }
</style>
