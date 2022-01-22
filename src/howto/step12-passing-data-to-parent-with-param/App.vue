<template>

<h2>This is Parent component</h2>
<button @click="showPopup = true">Show child component</button>

  <!--BT Step 3: Listen and event name: @closeme, then call the method -->
  <Popup v-show="showPopup" @closeme="callThisMethod" />

</template>

<script>

import Popup from './components/Popup.vue'

export default {

  name: 'App',

  //BT - Then register your component here using the name: Greet
  components:{

    Popup,
  },


  data(){

    return {
      showPopup: false
    }
  },
  methods: {
    //BT - Vue will automatically passed the data from the event automatically. (name)
    callThisMethod(name){
      this.showPopup = false
      //BT - This will log the data from the emit event from the child.
      console.log(name)
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
