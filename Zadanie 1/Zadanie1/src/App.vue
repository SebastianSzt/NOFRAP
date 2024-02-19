<template>
  <div id="app">
    <ExternalComponent />
  </div>
</template>

<script>
import ExternalComponent from './components/ExternalComponent.vue';

export default {
  components: {
    ExternalComponent
  }
};
</script>

<style>
  #app {
    font-family: 'Arial', sans-serif;
    text-align: center;
    margin-top: 20px;
  }
</style>
