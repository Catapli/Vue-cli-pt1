<template>
  <body>
    <div id="app">
        <h1>{{title}}</h1>
        <todo-list-vue v-bind:todos='todos'></todo-list-vue>
        <todo-add @add-new="addNew"></todo-add>
         <todo-delete-list @delete-all="delTodos"></todo-delete-list>
    </div>
</body> 
</template>

<script>
import TodoListVue from './components/TodoList.vue'
import TodoAdd from './components/TodoAdd.vue'
import TodoDeleteList from './components/TodoDeleteList.vue'

export default {
  name: 'App',
  components: {
    TodoListVue,
    TodoAdd,
    TodoDeleteList,
  },
  data(){
    return{
        title: 'Hello World',
        todos: [
            {
                id: 1,
                descrip: "Aprender Vue",
                done: false
            },
            {
                id: 2,
                descrip: "Dominar Vue",
                done: false
            }
    ],
    }
  },
  methods:{
    delTodos(){
        this.todos=[]
      },
      addNew(params){
        this.todos.push({id:6, descrip: params, done: false})
      },
      delTodo(index){
            console.log(index)
            //this.todos.splice(index,1);
        }
      
  }
  

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
