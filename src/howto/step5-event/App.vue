<template>

<h2>{{ name }}</h2>
<dir>
  <!-- BT - Calling a method without param, the Vue will automatically passed in the event and we can console.log it. 
            But if your method has a passed in param, then you must use a special keyword: $event as a second param and
            in your method, you must declare: event param to receive it. 
            Notes: You can also call multiple methods in the click event. Just separate it with a comma-->
  <button v-on:click="changeName($event),increment(5,$event)">Change me</button>
</dir>

<h2>{{ count }}</h2>
<div>
  <button v-on:click="increment(5, $event)">Increment</button>
  <!--BT - You can also use: @ instead of v-on -->
  <button @click="decrement()">Decrement</button>
</div>

</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'

export default {

  name: 'App',

  data(){
    return {
        name: "Trong",
        count: 0
      }
    },
  methods: {

    increment(num, event){
      this.count += num
      console.log(event)
    },
    decrement(){
      this.count -= 1
    },
    //BT - Vue is also automatically pass to us the event and we can console.log it to what event has happened.
    changeName(event){
      this.name = 'Bob'
      console.log(event)
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
