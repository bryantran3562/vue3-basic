<template>

  <h2>This is child component</h2>
  <!-- BT - SLOTS - Step 2: Then just declare a pair of slots HTML element below to receive data from the parent template -->
  <slot></slot>

</template>

<script>
export default {
  name: 'HelloWorld',

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
