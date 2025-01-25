<template>
    <div >
      <h1>Sum Number{{ 10+19 }}</h1>
      <h1>EmAIL {{ getData().email }}</h1>
      <h1>Name {{getName("maheshwor")}}</h1>
    </div>
  </template>
  
  <script>
  export default {
    name: 'HomeScreen',
    data(){
      return{
        email:'maheshwor@gmail.com',
      
      }
    },
    methods:{
      getName(name){
        return name;
      },
      getData(){
        return {
          name:'mahegd',
          email:'MAHESH@GMAIL.COM'
        }
      }
    }
  }
  </script>
  <style scoped>
  h1 {
    color: red;
  }
  </style>
  