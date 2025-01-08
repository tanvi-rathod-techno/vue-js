<template>
    <h1 v-on:mousemove="getConsole()">Home Components {{"Hello".length}}</h1>
    <h2>Email : {{email}}</h2>
    <h2>Mobile : {{mobile=123123}}</h2>
    <h2>Name : {{getName("Tanvi Rathod")}}</h2>
    <h2>User : {{userName("Tanvi Rathod")}}</h2>
    <h2>UserDeatils : {{getusername("Tanvi Rathod").email}}</h2>
    <button v-on:click="getData('button click ')">Click me</button>
    <button v-on:dblclick="getData('double button click ')">Double Click me</button>
    <h2>{{count}}</h2>
</template>
<script>
export default {

    name: "HomePage",
    email :"tanvi@gmail.com",
    data(){
        return {
            email :"tanvi@gmail.com",
            mobile :"132312312313",
            getName(x){
                return x
            },
            count :0
        }
    },
    methods:{
        userName(){
            return "Tanvi Rathod"
        },
        getusername(){
            return {
                name: "Tanvi",
                email: this.email
            }
        },
        getData(){
            this.count= this.count +1
        },
        getConsole(){
            console.log('event is fired');
        }
    }
}
</script>
<style scoped>
 h1{
    color:orange
 }
</style>