<template>

    <!-- BT - Props: Step1 - Defind a variable :sendDataToChild. The ':' is a data binding in which it allows you
                             to dynamically change the data with that defined variable -->
    <HelloWorld :sendDataToChild="sendDataToChild" />

</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data(){
    return {
      //BT - Props: Step 2 - Define your variable here and allows it to change dynamically. See step 3 in HelloWorld.vue (child component)
      sendDataToChild: "This data is from the Parent send to child"
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
