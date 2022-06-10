<template>
    <div class="disco">
        <div>{{dischiOggetto.title}}</div>
    </div>
</template>

<script>
export default {
  name: 'MyDisco',
  props: {
      dischiOggetto: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    #disco {
        background-color: rgb(38, 255, 0);
    }
</style>