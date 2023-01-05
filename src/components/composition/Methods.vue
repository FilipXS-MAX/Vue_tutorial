<template lang="">
    <div>
        <h2>{{name}}</h2>
        <button @click="setName">Change name</button>

        <h2>{{count}}</h2>
        <button @click="incrementCount">Increment count</button>

        
        <h2>{{first}} {{last}}</h2>
        <button @click="changeHero">Change hero</button>
    </div>
</template>

<script>
    import { ref, reactive, toRefs } from 'vue';

    export default {
        name: 'Methods',
        setup() {
            
            const count = ref(0);
            function incrementCount() {
                count.value++;
            }

            const state = reactive({
                first: 'Bruce',
                last: 'Wayne'
            })
            function changeHero() {
                state.first = 'Clark',
                state.last = 'Kent'
            }

            return {
                count,
                incrementCount,
                changeHero,
                ...toRefs(state)
            }
        },
        data() {
            return {
                name: 'Bruce'
            }
        },
        methods: {
            setName() {
                this.name = 'Test';
            }
        }
    }
</script>

<style lang="" scoped>
    
</style>