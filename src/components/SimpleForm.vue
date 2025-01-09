<template>
    <h1>Simple Form</h1>
    <form>
    <label for="Firstname"></label>
    <input type="text" placeholder="Firstname" v-model="form.Firstname"/>
    <label for="Lastname"></label>
    <input type="text" placeholder="Lastname" v-model="form.lastname"/>
    <button v-on:click="save">Save</button>
    </form>
</template>
<script>
export default{
    name :"SimpleForm",
    data(){
        return{
            form:{
            Firstname:'',
            Lastname:''
            }
        }
    }
}
</script>