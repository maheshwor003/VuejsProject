<template>
    <div >
        <input type="text" v-model="count">
        <h2>{{ count }}</h2>
   <button v-on:click="getName('alert clicked ');">Click</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'HomeScreen',
    data()
    {
        return{
            count:10
        }
    },
    methods:{
      getName(data){
        alert(data);
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
  