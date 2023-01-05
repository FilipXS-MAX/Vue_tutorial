<template lang="">
    <div>
        <input type="text" placeholder="First name" v-model="fName" />
        <input type="text" placeholder="Last name" v-model="lName" />
        
        <hr />
        
        <input type="text" placeholder="Hero name" v-model="heroName" />
        <input type="text" placeholder="First name" v-model="firstName" />
        <input type="text" placeholder="Last name" v-model="lastName" />
    </div>
</template>

<script>
    import { ref, reactive, toRefs } from 'vue';

    export default {
        name: 'VModel',
        setup() {
            const heroName = ref('')
            const state = reactive({
                firstName: '',
                lastName: ''
            })

            return {
                heroName,
                ...toRefs(state)
            }
        },
        data() {
            return {
                fName: '',
                lName: ''
            }
        },
        methods: {
            
        }
    }
</script>

<style lang="" scoped>
    
</style>