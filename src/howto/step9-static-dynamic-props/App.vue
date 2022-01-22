<template>


<!-- BT - Then place your component here in the App root to display in -->

  <!-- BT - Props - Sending data from Parent to child.
            Step1: Add an attribute to the child tag below with any key and value 
            See Step 2 in - Greet.vue file
            -->

  <Greet parentData="Jay" aka="Little Boy" :secondParam="dataPassToChild" />

</template>

<script>
//***************************************************************************************************************************** 
//BT - Note: Install Vue VSCode Snippet to help to create a vue file with - template, script and style portion automatically.
//            Create a new Greet.vue and then type:
//            vbase-css
//            It will then create all the needed parts for you in this file.
//***************************************************************************************************************************** 
//BT - Greet is the name of your component. Or, think import Greet component from ./components/Greet.vue file.
import Greet from './components/Greet.vue'

export default {

  name: 'App',

  //BT - Then register your component here using the name: Greet
  components:{
    Greet,
  },
  data(){
    //BT - You can also pass the data from here to the child component. But very important, you
    //     must do the colon for key as the above: <Greet parentData="Jay" aka="Little Boy" :secondParam="dataPassToChild" />
    //Otherwise, it will not work. This is call dynamic props.
    return {

      dataPassToChild: 'child data'

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
