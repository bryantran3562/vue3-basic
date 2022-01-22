<template>
    <div>

        <h2>Increment Number {{ num }}</h2>
        <button @click="Increment">Increment</button>
        <h2>Reactive Methods</h2>
        <h1>{{ first }} - {{ last }}</h1>
        <button @click="changeName">Change Name</button>

    </div>
</template>

<script>

import { ref, reactive, toRefs } from 'vue'
    export default {
        name: 'Method',
        setup(){

            const num = ref(0)

            //BT - All you have to do is named it as: function instead of method() in Option API
            //Note: There is no need - this - keyword when access the variable.
            function Increment(){
                num.value++
            }
            //######################################
            //BT - reactive function
            //######################################

            const state = reactive({
                first: 'trong',
                last: 'tran'
            })

            function changeName(){
                state.first = 'Jay'
                state.last = 'tran'
            }



            return {
                num,
                Increment,
                ...toRefs(state),
                changeName
            }
        }
    }
</script>

<style scoped>

</style>