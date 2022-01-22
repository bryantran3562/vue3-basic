<template>

<PostList />

</template>

<script>

//BT - Notes:  issue the command: npm add axios - to install the http get post supported.
//jsonplaceholder.typicode.com is a site for testing api json.

import PostList from './components/PostList.vue'

export default {

  name: 'App',

  //BT - Then register your component here using the name: Greet
  components:{

    PostList,

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
