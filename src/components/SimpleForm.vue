<template>
<div>
    <h2 v-bind="$attrs">Simple Form</h2>
</div>

<ul>
    <li v-for="item in error" v-bind:key="item">
        {{ item }} not valid
    </li>
</ul>

<br />
<br />
<form>
    <h1> {{ helloworldata   }}</h1>
    <label>Email: </label>
    <input type="text" placeholder="enter email" v-model.number.lazy="form.email">
    <br /> <br />
    <h2>Email : {{ form.email }}</h2>
    <h2>Data : {{ typeof(form.email)}}</h2>
    <label>Password: </label>
    <input type="password" placeholder="enter password" v-model.lazy="form.password">
    <br /> <br />
    <h2>password : {{ form.password }}</h2>
    <select v-model="form.country">
        <option>Nepal</option>
        <option>India</option>
        <option>China</option>
    </select>
    <h2>Gender</h2>
    <label for="maleid">Male</label>
    <input type="checkbox" v-model="form.gender" value="male" id="maleid" /><br><br>
    <label for="femaleid">Female</label>
    <input type="checkbox" v-model="form.gender" value="female" id="femaleid" />
    <br>
    <br>
    <h4>Selected Canidate:{{ form.gender }}</h4>
    <br>
    <br>

    <h2>Are you sure ?</h2>
    <label for="yees">Yes</label>
    <input type="radio" v-model="form.sureornot" name="status" value="yes" id="yees" />
    <label for="noo">No</label>
    <input type="radio" v-model="form.sureornot" name="status" value="no" id="noo" />
    <h4>{{ form.sureornot }}, I am preety sure This is {{ form.sureornot }}</h4>
    <br>

    <br>
    <button type="button" v-on:click="login">Login</button>
</form>
</template>

<script>
export default {
    name: "SimpleForm",
    props:{
                helloworldata:String
            },
    data() {
        return {
            form: {
                email: '',
                password: '',
                country: '',
                gender: [],
                sureornot: ''
            },
            error: []
           
        }
    },
    methods: {
        login() {
            this.error = [];
            for (const item in this.form) {
                if (this.form[item] === "" || this.form[item].length === 0) {
                    this.error.push(item)
                }
            }
            if (this.error.length === 0) {
                alert("data has been sumitted ");
            }

            console.log(this.form, this.error);
        }
    }

}
</script>

<style scoped>
h2 {
    color: orange;
}
</style>
