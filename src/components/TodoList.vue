<template>
    <div>
    
       <div v-for="(punkt,i) in list" :key="i">
      <TodoItem :punkt="punkt" :id="i" @delete-item="deleteItem"></TodoItem>
      
    </div> </div>
</template>

<script>
import TodoItem from "@/components/TodoItem";


    export default {
        name: 'TodoList',
        components: {
           TodoItem
        },
        props:{
            list: {
                type: Array
            }
        },
        methods: {
            deleteItem(i){
                this.$emit("delete-item", i);
            }
          },
     

        
    }  
</script>

<style>

</style>
