<template>
    <div>
    <ul>
          <Todoitem 
            v-for="todo of todos"
            v-bind:todo="todo"
          />
    </ul>  
    </div>
</template>

<script>
import Todoitem from './Todoitem.vue'
export default {
    props: ['todos'],
    components: {
        Todoitem
    }
}
</script>