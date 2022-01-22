<template>
    <div>
        <h2>Watcher with ref()</h2>
        <input type="text" v-model="first">
        <h2>Watcher with array input and with ref()</h2>
        <input type="text" v-model="name">
        <input type="text" v-model="age">
    </div>
</template>

<script>

import { ref, reactive, toRefs, watch } from 'vue'
    export default {
        name: 'Watcher',

        setup(){

            const first = ref('')
            //BT - watch() function with ref().
            //first: argument to watch
            //oldValue, newValue: These will automatically gives you these.
            watch(first,(oldValue, newValue) => {
                console.log(oldValue, newValue)
            })

            const name = ref('')
            const age = ref('')
            //BT - You can also watch with an array. The two oldValue, newValue will be access using array index based on the
            //     index of the array.
            watch([name, age], (oldValue, newValue) => {
                console.log(oldValue[0], newValue[0])
                console.log(oldValue[1],newValue[1])
            })


            return {
                first,
                name,
                age
            }
        }
    }
</script>

<style scoped>

</style>