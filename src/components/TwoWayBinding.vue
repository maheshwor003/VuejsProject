<template>
    <div >
     <h1>Two Way Binding </h1>
     <input type="text" v-model="count" />
     <h2>{{ count }}</h2>

     <input type="text" ref="input" />
     <button v-on:click="getData">highlight </button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'TwoWayBinding',
    data(){
      return{
      count:10
      
      }
    },
    methods:{
      getData(){
        this.$refs.input.focus();
        let val=this.$refs.input.value;
        console.warn(val);
        this.$refs.input.style.color="red"
      }
    
    }
  }
  </script>
  <style scoped>
  h1 {
    color: red;
  }
  </style>
  