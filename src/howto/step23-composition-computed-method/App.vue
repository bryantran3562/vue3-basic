<template>

<ComputedFunction />

</template>

<script>


import ComputedFunction from './components/ComputedFunction.vue'
export default {

  name: 'App',

  //BT - Then register your component here using the name: Greet
  components:{
      ComputedFunction

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
