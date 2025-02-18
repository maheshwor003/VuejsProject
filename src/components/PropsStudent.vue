<template>
    <div >
     <h1>Props in vue Js </h1>
     <h1>{{name}}</h1>
    </div>
  </template>
  
  <script>
  export default {
    name: 'PropsStudent',
    props:{
        name: String
    },
    data(){
    
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
  