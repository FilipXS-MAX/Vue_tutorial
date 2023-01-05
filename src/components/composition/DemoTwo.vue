<template lang="">
    <div>
        <h2>{{firstName}} {{lastName}}</h2>
        <h2>{{fName}} {{lName}}</h2>
    </div>
</template>

<script>
    import {reactive, toRefs} from 'vue';

    export default {
        name: 'DemoTwo',
        setup() {
            const state = reactive({
                firstName: 'Bruce',
                lastName: 'Twyne'
            })

            setTimeout(() => {
                state.firstName=  'Test';
                state.lastName = 'Test'
                console.log(state)
            }, 2000)

            return toRefs(state);

            // return {
            //     firstName: state.firstName,
            //     lastName: state.lastName
            // };
        },
        data() {
            return {
                fName: 'Bruce',
                lName: 'Twyne'
            }
        }
    }
</script>

<style lang="" scoped>
    
</style>