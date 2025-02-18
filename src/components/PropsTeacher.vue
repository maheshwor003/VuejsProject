<template>
<div>
    <h1>Props in Teacher vue Js </h1>
    <h1>teachername {{email}}</h1>
    <button v-on:click="getUser(userName)">Sent username </button>
</div>
</template>

  
<script>
export default {
    name: 'PropsTeacher ',
    props: {
        email: String,
        getUser:Function
    },
    data() {
        return {
            userName: "Peter"

        }
    }
}
</script>
  
<style scoped>
h1 {
    color: red;
}
</style>
