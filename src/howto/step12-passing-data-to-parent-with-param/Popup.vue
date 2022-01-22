<template>
    <div>
        <h2>This is child component</h2>
        <!--BT - Step 2: emit the event from the child to the Parent with the following format
                         "$emit('closeme')" <--At a click, emit the event named: closeme
                         See step 3 in App.vue.
                         You can also pass your data along with the event.
        -->
        <button @click="$emit('closeme','this data is from the child')">Close</button>

    </div>
</template>

<script>
    export default {

        name: 'Popup',
        //BT - Step 1: To send data from a child to a Parent, first:
        //emits: ['closeme'] <==Define an emit event and give it a name: closeme. This is the event that
        //                      Parent will listen to.
        emits: ['closeme']
            
               
    }
</script>

<style scoped>

</style>