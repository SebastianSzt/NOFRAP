<template>
  <div id="app">
    <user-list />
  </div>
</template>

<script>
  import UserList from './components/UserList.vue';

  export default {
    components: {
      UserList,
    },
  };
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    text-align: center;
    color: #a6b9c9;
    margin-top: 10px;
  }
</style>