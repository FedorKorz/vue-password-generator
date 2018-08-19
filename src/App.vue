<script>
  import PasswordBox from './components/PasswordBox';
  import RangeSlider from './components/RangeSlider';
  import LowerCaseVue from './store/LowerCase.vue';
  import CheckBoxes from './components/CheckBoxes';
  import UpperCase from './store/UpperCase';
  import LowerCase from './store/LowerCase';
  import Symbols from './store/Symbols';
  import Digits from './store/Digits';
  
  export default {
    components: {
      PasswordBox, RangeSlider, CheckBoxes
    },
    data: function(){
      return  {
        password: 'qwerty123',
        passwordLenght: 0,
        status: {
          symbolsInclude: true,
          uprInclude: true,
          digitsInclude: true,
          lwrInclude: true
        }
      }
    },
    methods: {
      generatePassword() {
        let password = [];
        let complexity = 0;

        for (let key in this.status) {
          (this.status[key]) ? complexity++ : [];
        }

        this.passwordLenght = document.getElementById("my-input").value;

        for (let i = 0; i < this.passwordLenght; i++) {
          let rndArr = Math.floor(Math.random() * complexity);

          switch (rndArr) {
            case 0:
              if (this.status.uprInclude) {
                password.push(UpperCase[Math.floor(Math.random() * UpperCase.length)]);
                break;
              }
            case 1:
              if (this.status.digitsInclude) {
                password.push(Digits[Math.floor(Math.random() * Digits.length)]);  
                break;
              }   
            case 2:
              if (this.status.symbolsInclude) {
                password.push(Symbols[Math.floor(Math.random() * Symbols.length)]);  
                break;
              } 
            case 3:
              if (this.status.lwrInclude) {
                password.push(LowerCase[Math.floor(Math.random() * LowerCase.length)]);  
                break;
              }
            }
        }
        this.password = password.join('');
      }
    }
  }
</script>

<template>
  <div class="app">
    <PasswordBox 
      @generatePass='generatePassword'
      v-bind:password='password'
      v-bind:passwordLenght='passwordLenght'>
    </PasswordBox>
    <RangeSlider 
      v-bind:password='password'
      @generatePass='generatePassword'
    />
    <CheckBoxes 
      v-bind:status="status"
    />
  </div>
</template>

<style>
  .app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    height: 600px;
    background-color: aquamarine;
  }
</style>
