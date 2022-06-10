<template>
    <div>
        <img :src="dischiObject.poster" alt="">
        <div>{{dischiObject.author}}</div>
    </div>
</template>

<script>
export default {
  name: 'MyDisco',
  props: {
      dischiObject: Object,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    div {
        background-color: aqua;
    }
</style>