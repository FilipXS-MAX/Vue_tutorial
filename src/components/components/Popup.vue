<template lang="">
    <div>
        <h2>This is popup</h2>
        <input v-model="name">
        <button @click="$emit('close', name)">Close popup</button>
    </div>
</template>

<script>
    export default {
        name: 'Popup',
        data() {
            return {
                name: ''
            }
        },
        methods: {

        },
        emits: {
            close: (name) => {
                if (!name) {
                    return false;
                } else {
                    return true;
                }
            }
        }
    }
</script>

<style lang="">
    
</style>