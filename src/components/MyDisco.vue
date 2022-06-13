<template>
    <div id="disco">
        <img :src="dischiObject.poster" alt="">
        <div id="testo">
            <h2>{{dischiObject.title}}</h2>
            <div class="autore_anno">
                <div>
                    {{dischiObject.author}}
                </div>
                <div>
                    {{dischiObject.year}}
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'MyDisco',
  props: {
      dischiObject: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    #disco {
        background-color: rgba(46,58,70,255);
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: center;
        width: 200px;
        margin: 30px;
        padding: 10px;
    }
     img {
        width: 170px;
    }
    
    #testo {
       display: flex;
       flex-direction: column;
       align-items: center;
       padding: 10px;
    }

    h2 {
        display: flex;
        flex-wrap: wrap;
        text-align: center;
        text-transform: uppercase;
    }

    .autore_anno {
        color: grey;
        text-align: center;
        padding-top: 10px;
    }
</style>