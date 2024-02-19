<template>
  <div>
    <p>Wewnętrzny Komponent: {{ internalValue }}</p>
    <button @click="changeInternalValue">Zmień Wartość</button>
  </div>
</template>
  
<script>
  export default {
    props: ['externalValue'],
    data() {
      return {
        internalValue: this.externalValue
      };
    },
    methods: {
      changeInternalValue() {
        this.internalValue += 1;
        this.$emit('valueChanged', this.internalValue);
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

  button {
    background-color: #4CAF50;
    color: white;
    border: none;
    padding: 10px 20px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    cursor: pointer;
  }

  button:hover {
    background-color: #45a049;
  }
</style>