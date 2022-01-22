<template>
    <div>
        <input type="text" v-model="heroName">
        <input type="text" v-model="first">
        <input type="text" v-model="last">
        <hr />
        <h1> {{ heroName }} {{ first }} {{ last }}</h1>
        
    </div>
</template>

<script>
import { ref, reactive, toRefs } from '@vue/reactivity'
    export default {
        name: "VModel",
        setup(){
            const heroName = ref('')

            const state = reactive({
                first: '',
                last:''
            })

            return {
                heroName,
                ...toRefs(state)
            }
        }
    }
</script>

<style scoped>

</style>