<template>
  <div id="app">
   <h1>to do application</h1>
   <TodoList 
   v-bind:todos="todos"
   @remove-todo="removeTodo"
   />
  </div>
</template>

<script>
import TodoList from '@/components/Todolist'
export default {
  name: 'App',
  data() {
    return {
      todos: [
        {id: 1, title: 'купить хлеб', completed: false},
        {id: 2, title: 'купить масло', completed: false},
        {id: 3, title: 'купить варенье', completed: false}
      ]
    }
  },
  methods:{
    removeTodo(id){
      this.todos = this.todos.filter(t => t.id !== id)
    }
  },
  components: {
    TodoList
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
