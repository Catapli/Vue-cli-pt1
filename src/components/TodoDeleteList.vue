<template>
    <button v-on:click="delTodos">Borrar lista</button>
</template>

<script>
export default {
    name:'delete-list',
    methods:{
        delTodos(){
      if(confirm('¿Deseas borrar la lista de cosas a hacer?')){
        this.$emit("delete-all")
      }
    },
    }
}
</script>