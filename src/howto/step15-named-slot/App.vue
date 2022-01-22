<template>
  <!-- BT - All you have to do is name it according to the slot name in the child component -->
  <Card>
    <template v-slot:header>This is data for header</template>
    <template v-slot:default>
      <img src="https://picsum.photos/200" alt="">
    </template>    
    <template v-slot:footer>This is data for header</template>    
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
