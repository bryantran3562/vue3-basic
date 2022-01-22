<template>

  <Card>This is data from Parent</Card>
  <Card><h2>This is data from Parent</h2></Card>
  <Card>
    <img src="https://picsum.photos/200" alt="">
  </Card>

</template>

<script>

import Card from './components/Card.vue'

export default {

  name: 'App',

  //BT - Then register your component here using the name: Greet
  components:{
      Card,
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
