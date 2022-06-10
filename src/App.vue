<template>
  <div id="app">
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
</style>
