<template>
    <div>
        <!--BT - Slot - All you have to do is include these Vue directive <slot></slot>
                        Then you can pass any html, text or evev image to this <slot></slot>
                        and it will display in between these. Slot is even more powerful than
                        props where you can only pass data -->
        <slot></slot>

    </div>
</template>

<script>
    export default {
        name: 'Card'
    }
</script>

<style scoped>

</style>