<template>
    <div>
        <h2>Article Component</h2>
        <h2>{{ title }} </h2>
        <h2>Likes - {{ likes }}</h2>
        <h2> Published {{ IsPublished ? 'Yes' : 'No'}} </h2>
        <h2>{{ noColon }}</h2>

    </div>
</template>

<script>
    export default {
        name: 'Artical',
        props: {
            //BT - You can also configure to have your props required. So, it will give you a warning in the browser if this props
            //     is missing from the parent. You can also configure it so that it will displaying a default string if the props is missing 
            //     from the parent, it will be displaying the default.
            title: {
                type: String,
                required: true,
                default: "This is a string by default"
            },
            likes: Number,
            IsPublished: Boolean,
            noColon: String
        }
    }
</script>

<style lang="scss" scoped>

</style>