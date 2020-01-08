<template>
  <div>
    <todo-input @emit2="emit3"></todo-input>
    <ul>
    <todo-item v-for="(item,index) in text2" :item="item" @click.native="remove(index)"></todo-item>
    </ul>
  </div>
</template>
<script>
import todoInput from "./todoInput.vue"
import todoItem from "./todoItem.vue"
export default {
    data(){
      return {
        text2:[],
      }
    },
    components:{
      todoInput,
      todoItem
    },
    methods:{
      emit3(addtodo){
        this.text2.push(addtodo)
      },
      remove(index){
        this.text2.splice(index,1)
      }
    }
}
</script>