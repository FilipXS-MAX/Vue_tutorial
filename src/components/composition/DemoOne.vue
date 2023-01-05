<template lang="">
    <div>
        <h2>{{name}}</h2>
        <h2>{{name2}}</h2>
    </div>
</template>

<script>
    import {ref} from 'vue';

    export default {
        name: 'DemoOne',
        setup() {
            let name = 'Filip'
            let name2 = ref('Filip');

            setTimeout(() => {
                name=  'Test';
                name2.value = 'Test'
                console.log(name, name2)
            }, 2000)

            return {
                name,
                name2
            };
        }
    }
</script>

<style lang="" scoped>
    
</style>