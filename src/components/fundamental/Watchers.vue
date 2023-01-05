<template lang="">
    <div>
        <h2>Volume Tracker (0-20)</h2>
        <h3>Current Volume : {{volume}}</h3>
        <div>
            <button @click="volume += 2">Increment</button>
            <button @click="volume -= 2">Decrement</button>
        </div>
        <div :style="{display: 'inline-flex'}">
            <input type="text" v-model="movie">
            <input type="text" v-model="movieInfo.title">
            <input type="text" v-model="movieInfo.actor">
        </div>

        <button 
            @click="movieList.push('Wonderwomen')"
            :style="{display: 'block',margin:'auto'}">
            Add movie
        </button>
    </div>
</template>
<script>
export default {
    data() {
        return {
            volume: 0,
            movie: '',
            movieInfo: {
                title: '',
                actor: ''
            },
            movieList: ["Superman", "Batman"]
        };
    },
    methods: {

    },
    computed: {

    },
    watch: {
        volume(newValue, oldValue) {
            console.log("Zmenil som volume: ", newValue)
            if (newValue > oldValue && newValue == 16 ) {
                alert("Pozor")
            }
        },
        movie: {
            handler(newValue) {
                console.log('Calling API with movie name = ', newValue)
            },
            // zaznamena sa aj inicializacia premennej (pri nacitani stranky)
            immediate: true
        },
        movieInfo: {
            handler(newValue) {
                console.log(`Calling API with movie title = ${newValue.title} and actor = ${newValue.actor}`)
            },
            // pri objektoch je potrebny tento atribut, inak sa nezaznamena zmena vnorenych prvkov
            deep: true
        },
        movieList: {
            handler(newValue) {
                console.log(`Update list ${newValue}`)
            },
            // to iste sa vyzaduje aj pri poliach
            deep: true
        }
    }
}
</script>
<style lang="">
    
</style>