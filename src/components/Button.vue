<template>
   <div >
    <button v-on:click="getData()">Click mee</button>
    <button v-on:dblclick="testbutton1('buttomnclicked')">Click mee</button>
    <h2>{{ count }}</h2>
   </div>
 </template>
 
 <script>
 export default {
   name: 'HomeScreen',
   data(){
     return{
      count:0
     
     }
   },
   methods:{
      getData()
      {
         this.count=this.count+1;
      },

     testbutton(){
      alert("Function is called !");

     },
     testbutton1(data){
      alert(data);
     },
     getDatas(){
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
 