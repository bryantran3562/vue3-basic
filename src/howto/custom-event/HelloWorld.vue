<template>
  <h2>This is child component</h2>
  <!-- BT - Custom Event - Step 1: Create a button and wire a function to it -->
  <button @click="sendEventToParent">Click Me to send data to Parent</button>

</template>

<script>
export default {
  name: 'HelloWorld',

  methods: {

    // BT - Custom Event: Step 2: Create a function to send an event to Parent
    sendEventToParent(){
        console.log('click me clicked...')
        // BT - This command will send an event to Parent. See step 3 in App.vue
        this.$emit('sendEventToParent')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
