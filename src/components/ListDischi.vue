<template>
    <div class="container">
        <MyDisco
            v-for="(element, i) in dischi" 
            :key="i"
            :dischiObject="element"
        />
    </div>
</template>

<script>
import axios from "axios"
import MyDisco from "./MyDisco.vue"

export default {
  name: 'ListDischi',
  components: {
    MyDisco
},
  data () {
      return {
          apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
          dischi: []
      }
  },
  created() {
      axios.get(this.apiUrl)
      .then(result => {
          this.dischi = result.data.response;
          console.log(result);
      })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .container {
        width: 70%;
        margin: auto;
        color: white;
        display: flex;
        justify-content: flex-start;
        flex-wrap: wrap;
    }

</style>