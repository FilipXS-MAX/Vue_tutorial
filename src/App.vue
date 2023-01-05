<template>
  <!-- <Fundamentals /> -->
  <!-- <Components /> -->
  <!-- <Http /> -->
  <Composition />
</template>

<script>
  import Components from './components/Components.vue';
  import Fundamentals from './components/Fundamentals.vue';
  import Http from './components/Http.vue';
  import Composition from './components/Composition.vue';

  /* eslint-disable vue/no-unused-components */
  export default {
    name: 'App',
    components: {
      Components,
      Fundamentals,
      Http,
      Composition
    }
  }
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.promoted {
  text-decoration: underline;
}

.sold-out {
  color: green;
}

.new {
  color: red;
}
</style>
