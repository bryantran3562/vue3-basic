<template>
    <div>
        <h2>Reactive Method</h2>
        <h1>{{ first }} - {{ last }} - {{ age }}</h1>
        <h2>{{ reactiveMesg }}</h2>

    </div>
</template>

<script>
import { reactive, toRefs } from '@vue/reactivity'
    export default {
        name: 'ToRef',
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
                //BT - In order not to have to access the following {{ state.first }} {{state.last }} {{state.age}}
                //     You must use the: toRefs() function. Then in the template above you can have the same access as the data() method
                //     {{ fist }} {{ last }} {{ age }}. See ReactiveMethod.vue
                ...toRefs(state),
                reactiveMesg
            }
                
            
        }
    }
</script>

<style scoped>

</style>