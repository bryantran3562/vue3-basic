<template>

    <h1>{{ title }}</h1>

    <HelloWorld />
  <!-- BT - SLOTs: Step 1: Create any custom HTML as below. -->
    <template-parent> This is template send from Parent using slots</template-parent>

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
