<template>
<div class="hello">
    <h1>{{ msg }}</h1>
    <SimpleForm helloworldata="Props Data pass to simple form" id="user-cmp" />

    <h1>Computed Property</h1>
    <h2>{{ getResult }}</h2>
    <h2>{{ getResultMethod() }}</h2>

    <h1>Watchers </h1>
    <h1>{{ count  }}</h1>
    <button v-on:click="count=count+1">(+)</button>
    <button v-on:click="count=count-1">(-)</button>
</div>
</template>

<script>
import SimpleForm from './SimpleForm.vue';
export default {
    name: 'HelloWorld',
    components: {
        SimpleForm
    },
    props: {
        msg: String
    },
    data() {
        return {
            dollor: 100,
            ruppesVal: 70,
            discount: 10,
            count: 0,
        }
    },
    watch: {
        count(val,prev) 
        {
            if (val > 5 && prev<val) {
               
                this.count=1;
            }
            if (val == 0) {
                alert(" Counting 0");
            }
        }
    },
    methods: {
        getResultMethod() {
            return (this.dollor * this.ruppesVal) - this.discount;
        }
    },
    computed: {
        getResult() {
            return (this.dollor * this.ruppesVal) - this.discount;
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style scoped>
h3 {
    margin: 40px 0 0;
}

ul {
    list-style-type: none;
    padding: 0;
}

li {
    display: inline-block;
    margin: 0 10px;
}

a {
    color: #42b983;
}
</style>
