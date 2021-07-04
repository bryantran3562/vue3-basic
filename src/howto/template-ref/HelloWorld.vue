<template>

  <h2>This is child component</h2>
  <input type="text" class="text" ref="name">
  <button @click="handleClick"></button>


</template>

<script>
export default {
  name: 'HelloWorld',
  methods: {
    handleClick(){
      //BT- Template ref is nothing more that - whenever you need to grap an HTML element, you can just give it
      //    ref="any_name_you_want". Then you can get that hanle by the method below.
      //Notes: classList is property of the javascript, it has nothing to do with Vue.
      //       add is a method of the java script. Then we add an 'active' class to this HTML element.
      
      this.$refs.name.classList.add('active')
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
