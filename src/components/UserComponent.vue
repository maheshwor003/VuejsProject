<template>
    <div class="solid">
      <p>{{data.name}} </p>
      <p>{{data.email}} </p>
      <button v-on:click="getname(data.name)">Alert Name</button>

      <button v-on:click="getItem(data.email)">Another from Parent Name</button>
    </div>
  </template>
  
  <script>

  export default {
    name: 'UserComponent',
    props:{
      data:Object,
      getItem:Function
    },
    methods:{
      getname(name)
      {
        alert(name);
      }
    }
  }
  </script>
  <style scoped>
  h1 {
    color: red;
  }
  .solid{
background-color: aqua;

  }
  </style>
  