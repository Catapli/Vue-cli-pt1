<template>
    <ul>
        <todo-item v-for="elem in todos" v-bind:elem="elem" :key="elem.id"></todo-item>
    </ul>
</template>

<script>
import TodoItem from './TodoItem.vue'
export default {
    name: 'list',
    props: ['todos'],
    methods:{
        delTodo(index){
            this.$emit('add-new',index)
        }
    },
    components:{
        TodoItem,
    }
}
</script>