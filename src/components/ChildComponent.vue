<template>
    <div >
     <h1>Child Component  </h1>
     <h1>{{name}} </h1>
     <h1>{{user.name}} </h1>
     <button v-on:click="getData()" >Call Function</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ChildComponent',
    props:{
      name:String,
      user:Object,
      getData:Function
    }
    }
   
  
  </script>
  <style scoped>
  h1 {
    color: red;
  }
  </style>
  