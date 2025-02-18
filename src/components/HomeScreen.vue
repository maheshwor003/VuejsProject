<template>
    <div >
      <h1>Sum Number{{ 10+19 }}</h1>
      <h1>EmAIL {{ getData().email }}</h1>
      <h1>Name {{getName("maheshwor")}}</h1>
      <h1 :class="{green:colourful,red:false}">CSS Binding </h1>

      <h1 :class="applyStyle">Use this by computed style</h1>

      <button v-on:click="colourful=!colourful"> Apply Color</button>
    </div>
  
    <li v-for="item in users" :key="item.name">
      <UserComponent :data="item" :getItem="getItem" />
    </li>

    <PropsStudent name="Maheshwor"/>
    
    <!-- <PropsTeacher :email="email"/> -->
    
    <PropsTeacher :getUser="getName" />
    
<div class="row" v-html="tag">

</div>
{{ text }}
  </template>
  
  <script>

  import UserComponent from './UserComponent.vue';
  import PropsStudent from './PropsStudent.vue';
  import PropsTeacher from './PropsTeacher.vue';
  export default {
    name: 'HomeScreen',
    components: {
      UserComponent,
      PropsStudent,
      PropsTeacher
    },
    data(){
      return{
        colourful:true,
        text:"Maheshwor",
        tag:"<h1>Maheshworssss</h1>",
        email:'maheshwoaar@gmail.com',
        users: [
          { name: "Maheshwor", email: "mahesh@gmail.com" },
          { name: "Ram", email: "ram@gmail.com" },
          { name: "Shyam", email: "shyam@gmail.com" },
          { name: "Test", email: "test@gmail.com" },
        ],
      
      }
    },
    computed:{
      applyStyle(){
        return{
          green:this.colourful,
          err:true,
          other:true
        }
      }
,
    },
    methods:{
      getName(userName){
        return userName;
      },
      getData(){
        return {
          name:'mahegd',
          email:'MAHESH@GMAIL.COM'
        }
      },
      getItem(email){
      alert(email);
      },
    }
  }
  </script>
  <style scoped>
  h1 {
    color: rgb(0, 0, 0);
  }
  .green{
    background-color: green;
    width: 200px;
  }
  .red{
    text-decoration: red;
    width: 200px;
  }
  </style>
  