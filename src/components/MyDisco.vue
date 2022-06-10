<template>
    <div class="disco">
        <img :src="dischiObject.poster" alt="">
        <div>{{dischiObject.title}}</div>
    </div>
</template>

<script>
export default {
  name: 'MyDisco',
  props: {
      dischiObject: Array
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    #disco {
        background-color: rgb(38, 255, 0);
    }
</style>