<template>
  <div id="app">
   <h1>to do application</h1>
   <TodoList 
   v-bind:todos="todos"
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
        {id: 1, title: 'купить хлеб', compiled: false},
        {id: 1, title: 'купить масло', compiled: false},
        {id: 1, title: 'купить варенье', compiled: false}
      ]
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
