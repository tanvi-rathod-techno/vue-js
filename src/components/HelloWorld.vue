<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>
    <Student name="Tanvi"/>
    <Teacher name="Tanvi Rathod"/>
    <child name="Rina"/>
       <child name="Siyaa" />
          <child name="DemoName"/>
      <watchers />
      <slot />
    <SimpleForm />
    <h1>Ref in Vue</h1>
    <input type="text" ref="input">
    <button v-on:click="getdata()">Ref Click</button>
    <Nonprops item="some data" name="Non-props component"/>
    <!-- <newData /> -->
</template>

<script>  
import Student from './Student.vue'
import Teacher from './Teacher.vue'
import SimpleForm from './SimpleForm.vue'
import Nonprops from './Nonprops.vue'
// import newData from './newData.vue'
import watchers from './watchers.vue'
import child from './child.vue'
import slot from './slot.vue'

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
        SimpleForm,
        Nonprops,
        // newData,
        watchers,
        child,
        slot
  }
}
</script>
