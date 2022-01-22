<template>

<div>{{ add(2,3,5) }} </div>

<!-- BT - using data from the data() - Note: the this keyword -->

<div>{{ multiply(10) }} </div>

</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'

export default {

  name: 'App',

  data(){
    return {
        multiplier: 5,
      }
    },
  methods: {
    add(a,b,c){
      return a+b+c
    },
    multiply(num){
      //BT - When using the data in the data(), must use this keyword.
      return num * this.multiplier
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
