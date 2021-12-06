<template>
    <form @submit.prevent="">
    <input v-model="nomDescrip"> 
    <button @click="addTodo">Añadir</button>
  </form>
</template>

<script>
export default {
    name: 'add-todo',
    data(){
        return{
            nomDescrip: '',
        }
    },
    methods:{
        addTodo() {
        this.$emit('add-new',this.nomDescrip)
    }
    }
}
</script>