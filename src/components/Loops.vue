<template>
    <div>
      <h1>Loops</h1>
      <ul>
        <li v-for="(item, index) in technology" :key="index">
          {{ item }}
        </li>
      </ul>
    </div>
  
    <div>
      <h1>Array of Objects</h1>
      <ul>
        <li v-for="user in users" :key="user.email">
          Name: {{ user.name }} | Email: {{ user.email }}
        </li>
      </ul>
    </div>
  
    <ChildComponent name="Maheshwor Shakha" :user="user" :getData="getData" />
  </template>
  
  <script>
  import ChildComponent from './ChildComponent.vue';
  
  export default {
    name: 'HomeScreen',
    components: {
      ChildComponent,
    },
    data() {
      return {
        technology: ["Java", "PHP", "Node"],
        users: [
          { name: "Maheshwor", email: "mahesh@gmail.com" },
          { name: "Ram", email: "ram@gmail.com" },
          { name: "Shyam", email: "shyam@gmail.com" },
          { name: "Test", email: "test@gmail.com" },
        ],
        user: { name: 'Mahe', email: 'test@gmail.com' },
      };
    },
    methods: {
      getData() {
        alert("Function is called!");
      },
    },
  };
  </script>
  
  <style scoped>
  h1 {
    color: red;
  }
  </style>
  