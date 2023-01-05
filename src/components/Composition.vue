<template lang="">
    <!-- <Data /> -->
    <!-- <DemoOne />
    <DemoTwo /> -->
    <!-- <Methods /> -->
    <!-- <Vmodel /> -->
    <!-- <Computed /> -->
    <!-- <Watch /> -->
    <!-- <ProvideInject /> -->
    <!-- <LifecycleC />
    <LifecycleO /> -->
    <!-- <TemplateRef /> -->
    <!-- <Person /> -->
    <ClickCounter />
    <HoverCounter />
</template>

<script>
    import Data from './composition/Data.vue'
    import DemoOne from './composition/DemoOne.vue';
    import DemoTwo from './composition/DemoTwo.vue';
    import Methods from './composition/Methods.vue';
    import Vmodel from './composition/Vmodel.vue';
    import Computed from './composition/Computed.vue';
    import Watch from './composition/Watch.vue';
    import ProvideInject from './composition/ProvideInject.vue';
    import LifecycleC from './composition/LifecycleC.vue';
    import LifecycleO from './composition/LifecycleO.vue';
    import TemplateRef from './composition/TemplateRef.vue';
    import Person from './composition/Person.vue';
    import ClickCounter from './composition/ClickCounter.vue';
    import HoverCounter from './composition/HoverCounter.vue';

    /* eslint-disable vue/no-unused-components */
    export default {
        name: 'Composition',
        components: {
            Data,
            DemoOne,
            DemoTwo,
            Methods,
            Vmodel,
            Computed,
            Watch,
            ProvideInject,
            LifecycleC,
            LifecycleO,
            TemplateRef,
            Person,
            ClickCounter,
            HoverCounter
        },
        data() {
            return {
            }
        },
    }
</script>

<!-- Scoped atribut zabezpecuje, ze sa styly aplikuju iba na dany komponent -->
<style scoped lang="css">
</style>