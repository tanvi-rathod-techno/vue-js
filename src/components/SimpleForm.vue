<template>
    <h1>Simple Form</h1>
    <ul>
    <li v-for="item in error" v-bind:key="item">
        {{item}} is not valid
    </li>
    </ul>
    <form>
    <label for="Firstname">First Name</label>
    <input type="text" placeholder="Firstname" v-model="form.firstname"/><br>
    <label for="Lastname">Last Name</label>
    <input type="text" placeholder="Lastname" v-model="form.lastname"/><br>
    <label for="Lastname">Male</label>
    <input type="radio" value="male" v-model="form.gender"/>
    <label for="Lastname">Female</label>
    <input type="radio" value="female" v-model="form.gender"/><br>
    <label for="technology">Java</label>
    <input type="checkbox" value="java" v-model="form.technology"/>
    <label for="technology">PHP</label>
    <input type="checkbox" value="php" v-model="form.technology"/>
    <label for="technology">Node</label>
    <input type="checkbox" value="node" v-model="form.technology"/><br>
     <select v-model="form.country">
     <option value="">India</option>
     <option>USA</option>
    </select><br>
    <button v-on:click="save" type="button">Save</button>
    </form>
</template>
<script>
export default{
    name :"SimpleForm",
    data(){
        return{
            form:{
            firstname:' ',
            lastname:' ',
            gender:" ",
            country:" ",
            technology:[]
            },
            error:[]
        }
    },
    methods:{
        save(){
            this.error = []
            console.log(this.form)
            for(const item in this.form){
                if(this.form[item] === " " || this.form[item].length === 0){
                    this.error.push(item)
                }
            }
            if(this.error.length === 0 ){
                alert("Data has been submitted");
            }
            console.warn(this.error)
        }
    }
}
</script>