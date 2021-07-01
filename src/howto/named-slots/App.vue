<template>

    <h1>{{ title }}</h1>

    <HelloWorld>
            <!-- BT - Named SLOTS - Step 1: It must be in between the child HTML. See HelloWorld.vue for Step 2 -->
            <template v-slot:fromParent> This is from Parent</template>

    </HelloWorld>




    

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
