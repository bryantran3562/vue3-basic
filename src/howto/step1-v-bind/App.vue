<template>

    <h1>{{ title }}</h1>

  <!--BT - You can also use v-text directive to display your data from the data() property -->

    <div v-text="name"></div>

    <!--BT - Binding to HTML attribute -->
    <h2 v-bind:id="headingId">This is a test</h2>
    <button v-bind:disabled="buttonDisabled">Button will be disabled</button>

    <!--BT - Binding to an HTML attribute - class 
            status: true or false
            'text_color': present in the <style> or not
            So, if true && text_color present in <style> then it will display red color.
            Otherwise, it will be 'false' no color. This is called conditioning apply
            class to an HTML attribute -->
    <div v-bind:class="status && 'text_color'">Underline Text</div>
    <!-- BT - You can also use if then elese -->
    <h2 v-bind:class="status ? 'text_color' : 'underline'">This is if then else class</h2>
    <!-- BT - You can also use object to conditioning your HTML class attribute.
               The idea is that: key == value pair, it will go and evaluate one by one then it will combine
               the result and apply the class attribute to it depencs on which key has the value set to true
                -->
    <h2 v-bind:class="{ 'text_color': status, 'underline': isSoldout}">This is object conditioning for the class</h2>

    <!-- BT - Binding to HTML attribute: style.
              VERY IMPORTANT: Think of the key is the elememt that will assigned to your style or class HTML attribute.
                              The value is either set or not set to that key
     -->
    <div v-bind:style="{ color: hightLightColor, 'font-size': fontSize }">This is using Style</div>

    <!--BT - You can also include your css object in the data() function and then bind it to the style class -->
    <div v-bind:style="objectBindingStyle">This is from the data function</div>


</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'

export default {

  name: 'App',
  data(){
    return {
      title: "This is Parent template",
      name: "Trong Tran",
      headingId: "heading",
      buttonDisabled: true,
      status: true,
      isSoldout: false,
      hightLightColor: 'blue',
      //BT - Note: You must append 'px' for it to work with px
      fontSize: 50 + 'px',
      objectBindingStyle: {
        color: 'red',
        fontSize: 50 + 'px'
      }
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
.underline{
  text-decoration: underline
}
.text_color{
  color: red;
}
</style>
