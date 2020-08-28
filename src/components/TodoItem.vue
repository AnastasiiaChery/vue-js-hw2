<template>
    <div>
    
      <span>{{punkt}}</span>
      <button @click="del(punkt)"> DELETE</button>
    </div>
    
</template>

<script>
  export default {
        name: 'TodoItem',
    props:{
            punkt: {
                type: Object
            }
        },
    methods:{
        del(el){
            this.$emit("delete-item",el);
        }
    }
      }
</script>

<style>

</style>
