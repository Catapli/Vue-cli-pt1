<template>
    <li>
        <input type="checkbox">
            <del v-if="elem.done">
                {{ elem.descrip }}
            </del>
            <span v-else>
                {{ elem.descrip }}
            </span>   
    </li>
</template>

<script>
export default {
    name: 'item',
    props: ['elem'],
    methods:{
        delTodo(index){
            this.todos.splice(index,1);
        }
    }
}
</script>