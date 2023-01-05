<template lang="">
    <div>
        <h2>{{2 + 3 + 5}}</h2>
        <h2>{{5 + 10 + 15}}</h2>
        <h2>Add method: {{add(2, 3, 5)}}</h2>
        <h2>Add method: {{add(5, 10, 15)}}</h2>
        <h2>Multiply method: {{multiply(baseValue)}}</h2>
        <br/>

        <h2>{{name}}</h2>
        <div>
            <button v-on:click="changeName('Batman', $event)" v-on:mouseover="changeName('Testo', $event)">Change name</button>
        </div>
        
        <h2>{{count}}</h2>
        <div>
            <button v-on:click="count += 1">Increment</button>
            <button v-on:click="count -= 1">Decrement</button>
        </div>
        <!-- v-on mozeme pisat skratene ako @ -->
        <div>
            <button @click="count += 5">Increment</button>
            <button @click="count -= 3">Decrement</button>
        </div>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                name: 'Filip',
                baseMultiplier: 5,
                baseValue: 2,
                count: 0
            }
        },
        methods: {
            add(a, b, c) {
                return a + b +c;
            },
            multiply(num) {
                return num * this.baseMultiplier;
            },
            changeName(name, event) {
                this.name = name;
                console.log(event)
            }
        }
    }
</script>
<style lang="">
    
</style>