<template lang="">
    <div class="card">
        <!-- slot element zobrazuje v3etko co je v tagoch componentu v parentovi, 
            ak tam nic nie je tak sa zobrazi default value -->
        <slot>Default value</slot>
        <div id="card-header">
            <slot name="header"></slot>
        </div>
        <div id="card-content">
            <slot name="content"></slot>
        </div>
        <div id="card-footer">
            <slot name="footer"></slot>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Card"
    }
</script>

<style lang="css">
    .card {
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
        transition: 0.3s;
        padding: 16px;
        margin-bottom: 20px;
        width: 200px;
    }
    .card:hover {
        box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
    }
</style>