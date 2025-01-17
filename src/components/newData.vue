<template>
    <h1>Computed</h1>
    <h2>{{getResult}}</h2>
</template>
<script>
export default {
    name:"newData",
    data(){
        return {
            dollers:100,
            rupeeval:70,
            discount:10
        }
    },
    computed:{
        getResult(){
            return (dollers * rupeeval) - discount
        }
    }
}
</script>