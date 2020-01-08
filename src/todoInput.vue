<template>
<div @click="addemit" @keydown.enter="addemit">
    <input type="text" v-model="addtodo">
    <button type="button">submit</button>
</div>
</template>
<script>
export default {
    data(){
        return {
            addtodo:""
        }
    },
    methods:{
        addemit(){
            if(this.addtodo == ""){
                return
            };
            this.$emit("emit2",this.addtodo);
            this.addtodo=""
        }
    }
 }
</script>