<template lang="en">
    <div>
        <h2 v-if="num == 0">The number is zero</h2>
        <h2 v-else-if="num < 0">The number is negative</h2>
        <h2 v-else-if="num > 0">The number is positive</h2>
        <h2 v-else>Not a number</h2>
    </div>
    <div v-if="display">
        <h2>Vishwas</h2>
        <h2>Codevolution</h2>
        <h2>Vue</h2>
    </div>

    <h2 v-show="showElement">Using v-show</h2>
    <h2 v-if="display">Using v-show</h2>
</template>

<script>
    export default {
        data() {
            return {
                num: null,
                display: false,
                showElement: false
            }
        },

    }
</script>

<style lang="en">
    
</style>