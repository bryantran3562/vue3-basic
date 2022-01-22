<template>

<h2>Hello {{ parentData }} {{ aka }} {{ secondParam }}</h2>

</template>

<script>
//BT - You need to name your component so that you can register it to your App component or Root Component.
export default {
  name: 'Greet',
  //BT - Define a props with a list of params that you will accepted from the parent.
  //     You can then use it in your template. Think of this as data that you have defined in data().
  props: ['parentData', 'aka','secondParam']

}
</script>

<style>

</style>
