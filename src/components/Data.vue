<template>
    <div>

        <h2>{{ name }}</h2>

        <h2>Composition method - {{ c_name }}</h2>

    </div>
</template>

<script>

import { ref } from 'vue'
    export default {
        name: 'Data',

        //BT - Composition API is another way to code the script block. It is trying to replace the Option API methods. Rather than having
        //     the data(), methods, computed properties, watcher, lifecycle hooks separate, with the Composition API, it is included all
        //     in the setup(). There are two ways to initialize your data.
        //ref('pass_in_your_primitive_type_here') <==Use this when declaring a single value.
        //reactive() <==Use this with an object variable.
        setup(){

            //BT - Step 1: Create a variable and then assigned it with a value 'Tran' string and then pass it to the ref().
            //             This in turn, create an object with your value and reference this object to your variable. So then
            //             when you want to change the value of that object, you must do: c_name.value = 'your_new_value'
            const c_name = ref('Tran')
            //BT - This is how you would assign a new value to it.
            c_name.value = 'Jay'

            //BT - Step 2: Then you must return it in order for the template to use it.
            return{
                c_name
            }

        },

        data(){
            return {
                name: 'Bryan'
            }
        }
    }
</script>

<style scoped>

</style>