<template>
    <div>
      <input 
        id='my-input'
        min='1'
        max='30'
        value='0'
        @input='generatePass()' 
        type='range'/>  
    </div>
</template>

<script>
  export default {
    methods: {
      generatePass() {
        this.$emit('generatePass');
      }
    }
  };
</script>

<style>
  #my-input {
    -webkit-appearance: none;
    width: 40%;
    height: 10px;
    border-radius: 5px;
    background: whitesmoke;
    outline: none;
    opacity: 0.7;
    -webkit-transition: .2s;
    transition: opacity .2s;
  }

  #my-input:hover {
    opacity: 1;
  }

  #my-input::-webkit-slider-thumb {
    -webkit-appearance: none;
    appearance: none;
    width: 15px;
    height: 15px;
    border-radius: 50%;
    background: teal;
    cursor: pointer;
  }
</style>
