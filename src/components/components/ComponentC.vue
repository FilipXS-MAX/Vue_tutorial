<template lang="">
    <h2>Component C</h2>
    <ComponentE />
</template>

<script>
    import ComponentE from './ComponentE.vue';

    export default {
        name:'ComponentC',
        components: {
            ComponentE
        },
        data() {
            return {

            };
        }
    }
</script>

<style lang="">
    
</style>