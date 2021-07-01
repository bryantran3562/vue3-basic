<template>

  <h1>{{ title }}</h1>

  <!-- BT - Custom Event: Step 3: This is how you listen to your child component event -->
    <HelloWorld @sendEventToParent="receiveEventFromChild" />

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
      title: "This is Parent template"
    }
  },

  methods: {
    // BT - Custom Event - Step 4: Received Event from child and use it in our template.
    receiveEventFromChild(){
      console.log(this.receiveEventFromChild)
      this.title = 'Data received from child component'
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
