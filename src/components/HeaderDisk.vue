<template>
  <header class="d-flex justify-content-between">
    <div><img src="https://storage.googleapis.com/pr-newsroom-wp/1/2018/11/Spotify_Logo_CMYK_Green.png" alt="spotify logo"></div>
    <select name="" id="">
      <option value="1">Rock</option>
      <option value="2">Metal</option>
      <option value="3">Jazz</option>
    </select>
  </header>
</template>

<script>
/* eslint-disable */

export default {
  name: 'HeaderDisk'
}
</script>

<style lang="scss" scoped>
  header{
    background-color: #2E3A46;
    color: white;
    padding: 1rem;

    img {
    width: 100px;
    }

    select{
      width: 100px;
      height: 1.5rem;
      border-radius: 5px;
    }
  }
</style>
