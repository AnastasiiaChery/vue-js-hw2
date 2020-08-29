<template>
    <div>
      <AddTodo @add-item="todoToArr"></AddTodo>
      <TodoList ></TodoList>
    <TodoList :list="list" @delete-item="deleteItem" />
    
    
    </div>
</template>

<script>
    import AddTodo from "@/components/AddTodo";
    import TodoList from "@/components/TodoList";
    
    export default {
        name: 'App',
        components: {
            AddTodo,
            TodoList
        },
     data(){
          return{
           list:[ ]
          }
        },
          methods: {
            todoToArr(ev){
                this.list.push(ev);
            },
            deleteItem(el){
                console.log(el);
                for (var i=0; i<this.list.length; i++)
                {
                    
                    if(this.list[i]==el)
                    {
                        
                        this.list.splice(i,1);
                    }
                }
            }
            },
       
    }
</script>

<style>

</style>
