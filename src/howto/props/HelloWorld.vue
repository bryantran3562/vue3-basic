<template>
  <h2>This is child component</h2>
  <!-- BT - Props - Step4: Then just used it in your template -->
  <h3>{{ sendDataToChild }}</h3>
</template>

<script>
export default {
  name: 'HelloWorld',
  //BT - Step 3: This is how you declare to receive the Props from the parent.
  props: {
    sendDataToChild: String
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
