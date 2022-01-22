<template>

<Data />

</template>

<script>

import Data from './components/Data.vue'
export default {

  name: 'App',

  //BT - Then register your component here using the name: Greet
  components:{
      Data,

  },


  data(){

    return {

    }
  },
  methods: {

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
