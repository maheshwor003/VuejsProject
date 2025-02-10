<template>
<div>
    <div v-if="show">
        <h1>Get Input Fileld </h1>
        <input type="text" placeholder="Enter username" v-model="username" /> <br><br>
        <input type="text" placeholder="Enter password" v-model="password" /> <br> <br>
        <Button v-on:click="getdata(username,password)" v-model="gender" type="button">GetVaules</Button>
        <h2>{{ count }}</h2>

    </div>

    <div v-else>
        <h2>Gender</h2>
        <label for="maleid">Male</label>
        <input type="checkbox" v-model="gender" value="male" id="maleid" /><br><br>
        <label for="femaleid">Female</label>
        <input type="checkbox" v-model="gender" value="female" id="femaleid" />
        <br>
        <br>
        <h4>Selected Canidate:{{ gender }}</h4>
        <br>
        <br>

        <h2>Are you sure ?</h2>
        <label for="yees">Yes</label>
        <input type="radio" v-model="sureornot" name="status" value="yes" id="yees" />
        <label for="noo">No</label>
        <input type="radio" v-model="sureornot" name="status" value="no" id="noo" />
        <h4>{{ sureornot }}, I am preety sure This is {{ sureornot }}</h4>
        <br>

        <br>
    </div>
    <br>

    <br>
    <button type="button" v-on:click="show=true">Show and Hide </button>
    <button type="button" v-on:click="show=!show">Toggle</button>
</div>
</template>

<script>
export default {
    name: 'GetInputValue',
    data() { //data haru define garna ko lagi 
        return {
            gender: [],
            sureornot: null,
            show: false
        }
    },
    methods: {
        ShowInputFields() {
            this.show=true;
               }

    }
}
</script>

<style scoped>
h1 {
    color: red;
}
</style>
