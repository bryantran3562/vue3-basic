<template>


  <Artical title="Artical 1" :likes="50" :IsPublished="true" :noColon="test" />


</template>

<script>

import Artical from './components/Artical.vue'

export default {

  name: 'App',

  //BT - Then register your component here using the name: Greet
  components:{

    Artical,
  },


  data(){

    return {
      test: "Testing no colon"
    }
  }

  

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
