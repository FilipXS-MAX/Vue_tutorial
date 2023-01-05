<template lang="">
    <div>
        <h2>Options - {{o_firstName}}</h2>

        <h2>Composition - {{c_firstname}}</h2>
        <h2>Composition - {{greet}}</h2>
        
        <h2>Composition - {{c_firstname}} {{c_lastName}} a.k.a. {{c_heroName}}</h2>
        <h2>Composition - {{greetHero}}</h2>
        
        <h2>Composition - {{state.firstName}} {{state.lastName}} a.k.a. {{state.heroName}}</h2>
        <h2>Composition - {{reactiveGreetHero}}</h2>
    </div>
</template>

<script>
    import { ref, reactive } from 'vue';

    export default {
        name: 'Data',
        setup() {
            const c_firstname = ref('Clark');
            const c_lastName = ref('Kent');
            const c_heroName = ref('Superman');

            c_firstname.value = 'Diana';
            const greet = `Hello ${c_firstname.value}`;
            const greetHero = `Hello ${c_firstname.value} ${c_lastName.value} a.k.a. ${c_heroName.value}`;

            const state = reactive({
                firstName: 'Princess',
                lastName: 'Diana',
                heroName: 'Wonder Woman',
            })

            const reactiveGreetHero = `Hello ${state.firstName} ${state.lastName} a.k.a. ${state.heroName}`;

            return {
                c_firstname,
                c_lastName,
                c_heroName,
                state,
                greet,
                greetHero,
                reactiveGreetHero
            };
        },
        data() {
            return {
                o_firstName: 'Bruce',
                o_lastName: 'Wayne',
                o_heroName: 'Batman',
            }
        },
    }
</script>

<!-- Scoped atribut zabezpecuje, ze sa styly aplikuju iba na dany komponent -->
<style scoped lang="css">
</style>