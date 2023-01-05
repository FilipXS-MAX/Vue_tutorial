<template lang="">
    <!-- <Createpost />
    <PostList /> -->
    <!-- <Parent /> -->
    <!-- <TemplateRef /> -->
    <ClickCounter />
    <HoverCounter />
</template>

<script>
    import PostList from './http/PostList.vue';
    import Createpost from './http/Createpost.vue';
    import Parent from './http/Parent.vue';
    import Child from './http/Child.vue'
    import TemplateRef from './http/TemplateRef.vue';
    import ClickCounter from './http/ClickCounter.vue';
    import HoverCounter from './http/HoverCounter.vue'

    /* eslint-disable vue/no-unused-components */
    export default {
        name: 'Http',
        components: {
            PostList,
            Createpost,
            Parent,
            Child,
            TemplateRef,
            ClickCounter,
            HoverCounter
        },
    }
</script>

<style lang="css">
    
</style>