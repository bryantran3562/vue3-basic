<template>

<!-- BT - Think of this as: if else statement - right side of the = will evaluate to true then it will exec. Otherwise,
          it will go to v-else. Note: if else must be next to each of other. -->

<div v-if="num === 0">First Line</div>
<div v-else-if="num > 0">Number is positive</div>
<div v-else-if="num < 0">Number is negative</div>
<div v-else>Not a number</div>

<!-- You can also using <template> tag. Use this <template> tag if there is an issue when you are using <div> tag.
     That could cause your layout issue.
 

<template v-if="num === -5">
  <h2>hi</h2>
  <h2>Trong Tran</h2>
</template>
-->

<!--BT v-show is the same as v-if -->

<h2 v-show="showIt">Using v-show</h2>



</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'

export default {

  name: 'App',

  data(){
    return {
        title: "This is a title",
        num: -5,
        showIt: true
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
