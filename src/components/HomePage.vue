<template>

    <h4>Move Event</h4> 
    ==============================
    <h1 v-on:mousemove="getConsole()">Home Components {{"Hello".length}}</h1>
   
    <h4>Interpolation</h4>
    ==============================
    <h2>Email : {{email}}</h2>
    <h2>Mobile : {{mobile=123123}}</h2>

    <h4>Methods,Function And Click Event</h4>    
    ==============================
    <h2>Name : {{getName("Tanvi Rathod")}}</h2>
    <h2>User : {{userName("Tanvi Rathod")}}</h2>
    <h2>UserDeatils : {{getusername("Tanvi Rathod").email}}</h2>
    <button v-on:click="getData('button click ')">Click me</button>
    <button v-on:dblclick="getData('double button click ')">Double Click me</button>

    <h4>Binding</h4>
    =============================
    <h2>{{count}}</h2>
    <input type="text" v-model="data">
    <h1>{{data}}</h1>
    <input type="text" placeholder="enter useremail" v-model="useremail"> <br>
    <input type="password" placeholder="enter password" v-model="password"> <br>
    <button v-on:click="getuserinputes()">Get Details</button>
    <br><br>

    <h4>Checkbox</h4>
    =============================
    <br>
    <label for="java">java</label>
    <input type="checkbox" value="java" id="java" v-model="technology" />
    <label for="node">Node</label>
    <input type="checkbox" value="node" id="node" v-model="technology" />
    <label for="php">PHP</label>
    <input type="checkbox" value="php" id="php" v-model="technology" />
    <h4>{{technology}}</h4><br>

    <h4>Radio</h4>
    =============================
    <br>
    <label for="student">Student</label>
    <input type="radio" value="student" id="student" name="profession" v-model="profession"/>
    <label for="developer">Developer</label>
    <input type="radio" value="developer" id="developer" name="profession" v-model="profession"/>
    <h4>{{profession}}</h4><br>


    <h4>If and else Condiction</h4>
    ============================
    <br>
    <h1 v-if="show">Hello If Condtions</h1>
     <h1 v-else>else in Vue js</h1>
    <button v-on:click="show=!show">Click Me</button>

    <h4>For Loop</h4>
    ============================
    <br>
    <ul>
      <li v-for="item in Looptechnology" :key="item"> {{item}}</li>
    </ul>
     <ul>
      <li v-for="item in users" :key="item.name">Name: {{item.name}} <br>Email: {{item.email}}</li>
    </ul>
  

  <child />
  <User/>
  <ul>
  <li ></li>
  </ul>

</template>
<script>
import child from './child.vue'
import User from './User.vue'
export default {

    name: "HomePage",
    email :"tanvi@gmail.com",
    components:{
        child,
        User
    },
    data(){
        return {
            email :"tanvi@gmail.com",
            mobile :"132312312313",
            getName(x){
                return x
            },
            count :0,
            data :0,
            useremail:null,
            password:null,
            technology:[],
            profession:null,
            show:true,
            Looptechnology:[
                'java',
                'php',
                'html',
                'node',
                'vuejs'
            ],users:[
                {
                name:"tanvi",
                email:"tanvi@gmail.com"
                },
                {
                name:"riya",
                email:"riya@gmail.com"
                },
                {
                name:"meera",
                email:"meera@gmail.com"
                },
            ]
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
        },
        getuserinputes(){
            console.log('values',this.useremail,this.password);
        }

    }
}
</script>
<style scoped>
 h1{
    color:orange
 }
</style>