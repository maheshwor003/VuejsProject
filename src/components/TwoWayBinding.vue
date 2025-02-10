<template>
    <div >
     <h1>Two Way Binding </h1>
     <input type="text" v-model="count" />
     <h2>{{ count }}</h2>
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
    
    }
  }
  </script>
  <style scoped>
  h1 {
    color: red;
  }
  </style>
  