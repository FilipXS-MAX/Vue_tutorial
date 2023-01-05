<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div>{{ greet }} {{ name }}</div>
    <div v-text="channel"></div>
    <div v-html="channel"></div>
    <div v-html="hack"></div>
    <!-- <div v-text="name">Hello</div> toto nefunguje-->

    <h2 v-bind:id="headingId">Heading</h2>
    <h2 class="static-class" v-bind:class="isPromoted && 'promoted'">Heading</h2>
    <h2 class="static-class" v-bind:class="isSoldout ? 'sold-out' : 'new'">Soldout</h2>
    <button v-bind:disabled="isDisabled">Bind</button>

    <h2 v-bind:class="['new','promoted']">Promoted</h2>
    <h2 v-bind:class="[isPromoted && 'promoted',isSoldout ? 'sold-out' : 'new']">Extra Promoted</h2>
    <h2 v-bind:class="{
        promoted: isPromoted,
        new: !isSoldout,
        'sold-out': isSoldout
    }">Promoted</h2>

    <h2 v-bind:style="{
        color: highlightColor,
        fontSize: headerSize + 'px',
        padding: '20px'
    }">Inline style</h2>
    <h2 v-bind:style="headerStyleObject">Inline style</h2>
    <h2 v-bind:style="[headerStyleObject, successStyleObject]">Inline style</h2>

    <!-- v-bind sa casto pouziva tak preto sa pouziva skor skratena verzia -->
    <h2 :style="[headerStyleObject, successStyleObject]">Inline style</h2>
</template>

<script>

export default {
    data() {
        return {
            greet: "Ahoj",
            name: "Batman",
            channel: "<b>Codevolution</b>",
            hack: `<a href="#" onclick="alert('You have been hacked!')">Win a prize!</a>`,
            headingId: "heading",
            isDisabled: true,
            status: "success",
            isPromoted: true,
            isSoldout: true,
            highlightColor: "orange",
            headerSize: 50,
            headerStyleObject: {
                color: 'orange',
                fontSize: '50px',
                padding: '20px'
            },
            successStyleObject: {
                color: 'green',
                backgroundColor: 'lightgreen',
                border: '1px solid green'
            }
        }
    }
}
</script>

<style>

</style>