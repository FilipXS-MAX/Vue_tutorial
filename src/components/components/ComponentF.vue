<template lang="">
    <h2>Component F</h2>
    <h2>Component F: {{username}}</h2>
</template>
<script>
export default {
    name:'ComponentF',
    data() {
        return {

        };
    },
    inject: ['username']
}
</script>
<style lang="">
    
</style>