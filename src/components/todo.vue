<template>
  <input type="text" value="todo.text" @keyup.enter="addTodo()">
    <li v-for="todo in todos">{{todo.text}}</li>
</template>


<script>
  import store from './store'

  export default {
    computed: {
      todos () {
        return store.state.todos
      }
    }
  }
</script>
