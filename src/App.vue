<template>
  <div id="app">
    <MyMain/>
  </div>
</template>

<script>
import MyMain from './components/MyMain.vue'

export default {
  name: 'App',
  components: {
    MyMain,
}
}
</script>

<style>
  *{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }
</style>
