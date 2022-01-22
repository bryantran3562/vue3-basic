<template>

<Watcher />

</template>

<script>


import Watcher from './components/Watcher.vue'
export default {

  name: 'App',

  //BT - Then register your component here using the name: Greet
  components:{
      Watcher

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
