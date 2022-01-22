<template>
    <div>
        
        <!--BT - Step 4: Configure click event to call our own function getPosts() -->
        <button @click="getPosts">Fetch Data</button>
        <h2 v-if="msgError">{{ msgError }} </h2>
        <div v-for="post in posts" :key="post.id">
            <h2>{{ post.id }} {{ post.title }}</h2>
            <p> {{ post.body }}</p>
            <hr />
        </div>

    </div>
</template>

<script>
//BT - Step 1: Import axio package.
import axios from 'axios'
    export default {
        name: 'PostList',
        data(){
            return {
                //BT - Step 2: This is for store our incoming data.
                posts: [],
                msgError: ''
            }
        },
        methods: {
            //BT - Step 3: Create a method to fetch the data using axios
            getPosts(){
                axios.get('https://jsonplaceholder.typicode.com/postsafd')
                .then((response) => {
                    //BT - Store data into our variable
                    this.posts = response.data
                    //BT - Log to the console
                    console.log(response.data)
                })
                .catch((error)=>{
                    console.log(error)
                    this.msgError = "Error retrieving the data"
                })
            }
        }
    }
</script>

<style scoped>

</style>