<template>
    <div>
        <h2>Reactive Method</h2>
        <h1>{{ state.first }} - {{ state.last }} - {{ state.age }}</h1>
        <h2>{{ reactiveMesg }}</h2>

    </div>
</template>

<script>
import { reactive } from '@vue/reactivity'
    export default {
        name: 'ReactiveMethod',
        setup(){
            //BT - Step 1: reactive() is exactly the same as the ref() function. Except that it accepted an object instead of one variable.
            // The convention is declare a - const state and assigned the reactive method to it.
            const state = reactive({
                first: 'Trong',
                last: 'Tran',
                age: 58
            })
            //BT - Step 2: This is how to access its member.
            const reactiveMesg = `Hello ${state.first} - ${state.last} - ${state.age}`

            return {
                state,
                reactiveMesg
            }
        }
    }
</script>

<style scoped>

</style>