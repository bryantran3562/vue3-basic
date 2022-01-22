<template>
    <div>
        <h2>Ref with computed Function</h2>
        <input type="text" v-model="first">
        <input type="text" v-model="last">
        <h2>Ref {{ refComputedFunction }}</h2>

        <h2>Reactive with computed Function</h2>
        <input type="text" v-model="reactiveFirst">
        <input type="text" v-model="reactiveLast">
        <h2>Reactive: {{ reactiveComputedFunction }}</h2>

    </div>
</template>

<script>

import { ref, reactive, toRefs, computed } from 'vue'
    export default {
        name: 'ComputedFunction',
        setup(){
            const first = ref('')
            const last = ref('')
            //BT - ref() with computed method
            const refComputedFunction = computed(function() {
                return `${first.value} ${last.value}`
            })

            //BT - reactive() with computed method.
            const state = reactive({
                reactiveFirst: '',
                reactiveLast: ''
            })

            const reactiveComputedFunction = computed(function(){
                return `${state.reactiveFirst} - ${state.reactiveLast}`
            })


            return{
                first,
                last,
                refComputedFunction,
                ...toRefs(state),
                reactiveComputedFunction
            }
        }
    }
</script>

<style scoped>

</style>