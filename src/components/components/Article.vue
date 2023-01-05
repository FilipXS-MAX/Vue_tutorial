<template lang="">
    <!-- id komponentu sa automaticky priradi divu, ak tu div nie je tak sa nepriradi nikde -->
    <div>
        <!-- manualne ale vieme priradit id jednotlivym elementom pomocou v-bind -->
        <h2 v-bind="$attrs">Article component</h2>
        <h2>{{ title }}</h2>
        <h2>Likes: {{ likes }}</h2>
        <h2>Published: {{ isPublished ? 'Yes':'No' }}</h2>
    </div>
</template>
<script>
export default {
    name: 'Article',
    props: {
        title: {
            type: String,
            required: true,
            // defaultna hodnota, ak tuto premennu nevlozime do componentu
            default: 'Article default title',
        },
        likes: Number,
        isPublished: Boolean
    },
    inheritAttrs: false,
    data() {
        return {

        }
    },
    methods: {

    }
}
</script>
<style lang="">
    
</style>