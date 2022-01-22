<template>
    <div>
        <h2>Create List</h2>
        <form @submit.prevent="createList">
            <label for="userid">User Id</label>
            <input type="text" v-model="formData.userId">
            <label for="title">Title</label>
            <input type="text" v-model="formData.title">
            <label for="body">Body</label>
            <input type="text" v-model="formData.body">
            <button>Submit</button>
        </form>
    </div>
</template>

<script>
import axios from 'axios'
    export default {
        name: 'CreateList',
        data(){
            return {
                //BT - Step 1: Create an object to hold our user input.
                formData: {
                    userId: '',
                    title: '',
                    body: ''
                }
            }
        },
        methods: {
            createList(){
                axios.post('https://jsonplaceholder.typicode.com/posts', this.formData)
                .then(response => console.log(response))
                .catch(error => console.log(error));
            }
        }
    }
</script>

<style scoped>

</style>