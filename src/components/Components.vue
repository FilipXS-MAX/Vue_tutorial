<template lang="">
    <!-- <Greet name="Bruce" heroName="Batman" />
    <Greet name="Clark" heroName="Superman" />
    <!- - mozeme pouzit tak ako to mame definovane - ->
    <Greet name="Diana" hero-name="Hulk" />
    <Greet :name="name" :heroName="channel" /> -->

    <!-- <Article id="my-article" title="Article Title" :likes="5" :isPublished="false" /> -->
    <!-- <h3>Username app: {{username}}</h3>
    <button @click="this.username = 'Test'">Change username</button>
    <ComponentC /> -->
    <!-- <button @click="showPopup=true">Show Popup</button>
    <Popup v-show="showPopup" @close="closePopup" /> -->
    <!-- <Input v-model="name" /> -->

    <!-- <Card></Card>
    <Card>Card content</Card>
    <Card>
        <img src="@/assets/logo.png" />
    </Card>
    <Card>
        <template v-slot:header>
            <h3>Header</h3>
        </template>
        <template v-slot:content>
            <h3>Content</h3>
        </template>
        <template v-slot:footer>
            <h3>Footer</h3>
        </template>
        <template v-slot:default>
            <h3>Default</h3>
        </template>
    </Card> -->
    <!-- <NameList>
        <template v-slot:default="slotProps">
            {{slotProps.firstName}} {{slotProps.lastName}}
        </template>
    </NameList>
    <NameList>
        <template v-slot:default="slotProps">
            {{slotProps.lastName}}, {{slotProps.firstName}}
        </template>
    </NameList>
    <NameList>
        <template v-slot:default="slotProps">
            {{slotProps.firstName}}
        </template>
    </NameList> -->

    <!-- <h4>Parent styles</h4>
    <ChildStyles /> -->

    <!-- <button @click="activeTab = 'TabA'">Tab A</button>
    <button @click="activeTab = 'TabB'">Tab B</button>
    <button @click="activeTab = 'TabC'">Tab C</button>
    <!- - <TabA v-if="activeTab == 'TabA'" />
    <TabB v-if="activeTab == 'TabB'" />
    <TabC v-if="activeTab == 'TabC'" /> - ->
    <!- - keep-alive element nechava nazive element, ktore sa vypinaju, v nom nemozu byt komentare - ->
    <!- - element component prepina medzi komponentami podla nazvu premennej - ->
    <keep-alive>
        <component :is="activeTab" />
    </keep-alive> -->
    <teleport to="#portal-root">
        <Portal />
    </teleport>
</template>

<script>
    import Greet from './components/Greet.vue';
    import Article from './components/Article.vue';
    import ComponentC from './components/ComponentC.vue';
    import Popup from './components/Popup.vue';
    import Input from './components/Input.vue';
    import Card from './components/Card.vue';
    import NameList from './components/NameList.vue';
    import ChildStyles from './components/ChildStyles.vue';
    import TabA from './components/TabA.vue'
    import TabB from './components/TabB.vue'
    import TabC from './components/TabC.vue'
    import Portal from './components/Portal.vue';

    /* eslint-disable vue/no-unused-components */
    export default {
        name: 'Components',
        components: {
            Greet,
            Article,
            ComponentC,
            Popup,
            Input,
            Card,
            NameList,
            ChildStyles,
            TabA,
            TabB,
            TabC,
            Portal
        },
        data() {
            return {
                name: 'Vishwas',
                channel: 'Codevolution',
                username: 'Filip',
                showPopup: false,
                activeTab: 'TabA'
            }
        },
        methods: {
            closePopup(name) {
                this.showPopup = false;
                console.log(name)
            }
        },
        provide() {
            return {
                username: this.username
            }
        }
    }
</script>

<!-- Scoped atribut zabezpecuje, ze sa styly aplikuju iba na dany komponent -->
<style scoped lang="css">
    h4 {
        color: orange
    }
</style>