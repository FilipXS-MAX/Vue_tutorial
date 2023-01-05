<template lang="">
    <div>
        Hello {{name}} a.k.a. {{heroName}}
    </div>
</template>
<script>
export default {
    name: "Greet",
    // input premenne
    props: ['name', 'heroName']
}
</script>
<style lang="">
    
</style>