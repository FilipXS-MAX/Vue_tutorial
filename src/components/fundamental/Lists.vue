<template lang="">
    <div>
        <h2 v-for="(name, index) in names" :key="name">{{index}} {{name}}</h2>
        <br/>
        <h2 v-for="(name, index) in fullNames" :key="name.first">
            {{index}} {{name.first}} {{name.last}}
        </h2>
    </div>
    <br/>
    <div v-for="actor in actors" :key="actor.name">
        <h2>{{actor.name}}</h2>
        <h3 v-for="movie in actor.movies" :key="movie"> {{movie}}</h3>
    </div>
    <br/>
    <div>
        <h2 v-for="(value, key, index) in myInfo" :key="value">{{index}}. {{key}}: {{value}}</h2>
    </div>
    <br/>

    <template v-for="name in names" :key="name">
        <h2>{{name}}</h2>
        <input placeholder="Last name" />
        <hr/>
    </template>
    <button @click="shuffle">Shuffle!</button>
    
    <!-- v-if a v-for nemoze byt v jednom elemente -->
    <template v-for="name in names" :key="name">
        <h2 v-if="name == 'Bruce'">{{name}}</h2>
    </template>
</template>
<script>
    import _ from "lodash"

    export default {
        data() {
            return {
                names: ['Bruce', 'Clark', 'Diana', 'Barry'],
                fullNames: [
                    { first: 'Clark', last: 'Wayne'},
                    { first: 'Bruce', last: 'Kent'},
                    { first: 'Princess', last: 'Diane'}
                ],
                actors: [
                    {
                        name: 'Cristian Bale',
                        movies: ['Batman', 'The Prestige']
                    },
                    {
                        name: 'Di Caprio',
                        movies: ['Titanic', 'Inception']
                    }
                ],
                myInfo: {
                    name: 'Filip',
                    channel: 'Codevolution',
                    course: 'Vue 3'
                }
            }
        },
        methods: {
            shuffle() {
                console.log(this.names)
                this.names = _.shuffle(this.names);
            }
        }
    }
</script>
<style lang="">
    
</style>