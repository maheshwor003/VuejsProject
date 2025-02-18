<template>
<!-- <img alt="Vue logo" src="./assets/logo.png"> -->
<HelloWorld msg="Welcome to Maheshwor Vue Js" />
<SimpleForm />
<!-- <HomeScreen  />
<GetInputValue/>
 <Button /> 
<TwoWayBinding/>
<Loops/> -->
</template>

<script>
 import HelloWorld from './components/HelloWorld.vue'
  import SimpleForm from './components/SimpleForm.vue'
  
// import HomeScreen from './components/HomeScreen.vue'
// import Button  from './components/Button.vue';
// import TwoWayBinding  from './components/TwoWayBinding.vue';
// import GetInputValue  from './components/GetInputValue.vue';
// import Loops  from './components/Loops.vue';


export default {
    name: 'App',
    components: {
        HelloWorld,
        SimpleForm
      //   HomeScreen,
        // Button,
      //   TwoWayBinding,
      //  GetInputValue,
      //  Loops
    }
}
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
 
    color: #2c3e50;
    margin-top: 60px;
}
</style>
