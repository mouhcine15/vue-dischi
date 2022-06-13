<template>
    <div class="container">
        <select id="generi" name="" form=""  v-model="userSelect" @click.prevent="$emit('selected', userSelect)">
            <option value="all">All</option>
            <option value="Rock">Rock</option>
            <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option>
            <option value="Metal">Metal</option>
        </select>
    </div>
</template>

<script>

export default {
  name: 'MySearch',
    data () {
      return {
          userSelect: "",
      }
  },
  created() {
      
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>