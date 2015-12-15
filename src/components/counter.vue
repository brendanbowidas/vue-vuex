<template>
  <div class="container">
    <h2>Clicked {{count}} times</h2>
    <button @click="increment">+</button>
    <button @click="decrement">-</button>
  </div>
</template>

<script>
  import store from '../store.js'

    export default {
      computed: {
        count () {
          return store.state.count
        }
      },
      methods: {
        increment: store.actions.increment,
        decrement: store.actions.decrement
      }
    }

</script>
