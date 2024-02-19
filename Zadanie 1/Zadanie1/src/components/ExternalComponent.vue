<template>
  <div>
    <p>Zewnętrzny Komponent: {{ externalValue }}</p>
    <InternalComponent :externalValue="externalValue" @valueChanged="handleInternalValueChange" />
  </div>
</template>
  
<script>
  import InternalComponent from './InternalComponent.vue';
  
  export default {
    data() {
      return {
        externalValue: 0
      };
    },
    components: {
      InternalComponent
    },
    methods: {
      handleInternalValueChange(newValue) {
        this.externalValue = newValue;
      }
    }
  };
</script>
  
<style scoped>
  div {
    border: 1px solid whitesmoke;
    padding: 10px;
  }

  p {
    font-size: 18px;
    margin-bottom: 10px;
  }
</style>