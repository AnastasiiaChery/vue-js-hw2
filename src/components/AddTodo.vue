<template>
    <div>
    
     <input type="text" v-model="newPunkt">
     <button @click="AddItem">SAVE </button>
    </div>
</template>

<script>
      
    export default {
        name: 'AddTodo',
        props:{
            list: {
                type: Array
            },
      },
      data() {
        return {
          newPunkt: "",
        }
      },
      methods: {
        AddItem() 
        {
          console.log(this.newPunkt);
          this.$emit("add-item",this.newPunkt);
          this.newPunkt = "";
        }
      }
      
       
        
    }

</script>

<style>

</style>
