<template>
    <div>
        <div id="selector">
            <div>
                <MySearch @selected="selectUser"/>

            </div>
        </div>
        <div class="container">
            <MyDisco
                v-for="(element, i) in filtroGeneri" 
                :key="i"
                :dischiObject="element"
            />
        </div>
    </div>
</template>

<script>
import axios from "axios"
import MyDisco from "./MyDisco.vue"
import MySearch from "./MySearch.vue"

export default {
  name: 'ListDischi',
  components: {
    MyDisco,
    MySearch
},
  data () {
      return {
          apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
          dischi: [],
          selected: ''
      }
  },
  created() {
      axios.get(this.apiUrl)
      .then(result => {
          this.dischi = result.data.response;
          console.log(result)
      })
  },
  computed: {
    filtroGeneri() {
        if (this.selected === "all") {
            return this.dischi
        }
        return this.dischi.filter((item) => {
            return item.genre.includes(this.selected)
        })
    }
  },

  methods: {
    selectUser(selezione){
        this.selected = selezione
    }
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

    #selector {
        margin-top: 10px;
        display: flex;
        justify-content: center;
    }

</style>