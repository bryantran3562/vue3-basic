<template>
    <div>
        <!--BT - You can named your slot so that the Parent knows which one is which to send data to -->
        <div id="header">
            <slot name="header"></slot>
        </div>
        <div id="default">
            <!--BT - Slot without a name is call default slot -->
            <slot></slot>
        </div>
        <div id="footer">
            <slot name="footer"></slot>
        </div>        
    </div>
</template>

<script>
    export default {
        name: 'Card'
    }
</script>

<style scoped>

</style>