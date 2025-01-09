<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>
    <Student name="Tanvi"/>
    <Teacher name="Tanvi Rathod"/>

    <SimpleForm />
    <h1>Ref in Vue</h1>
    <input type="text" ref="input">
    <button v-on:click="getdata()">Ref Click</button>
</template>

<script>
import Student from './Student.vue'
import Teacher from './Teacher.vue'
import SimpleForm from './SimpleForm.vue'
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    
  },
  methods:{
      getdata (){
     this.$refs.input.focus();
     this.$refs.input.value = "Vue js Ref";
    }
  },
  components:{
        Student,
        Teacher,
        SimpleForm
  }
}
</script>
