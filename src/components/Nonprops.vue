<template>
    <h1>Non- Props Component</h1>
    <h3>Bruce</h3>
    <h3>herry</h3>
    <h3>Tony</h3>
   <h3>{{item}}</h3>
    <!-- <h3 v-bind="$attr"></h3> -->
</template>
<script>
export default {
    name:"Nonpros",
    props:{
        item:String
    }
}
</script>