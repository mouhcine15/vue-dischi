<template>
  <div id="app">
    <div class="top">
      <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Spotify_logo_without_text.svg/768px-Spotify_logo_without_text.svg.png" alt="">
    </div>

    <ListDischi/>
  </div>
</template>

<script>
import ListDischi from './components/ListDischi.vue'

export default {
  name: 'App',
  components: {
    ListDischi
}
}
</script>

<style>
  *{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }

  #app {
    background-color: rgba(30,45,59,255);
    height: 100vh;
  }

  .top {
    background-color: rgba(46,58,70,255);
    height: 80px;
    display: flex;
    align-items: center;
  }

  .top img {
    width: 60px;
    margin-left: 20px;
  }
</style>
