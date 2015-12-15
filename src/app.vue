<template>
    <p class="red">{{msg}}</p>
    <clicker></clicker>
    <products></products>
    <alert type="error">Error message</alert>
    <alert type="success">Success message</alert>
    <counter></counter>
</template>


<style lang="sass">
    .red{
        color: red;

        &:hover{
            color: blue;
        }
    }
</style>


<script>

    require('./scss/main.scss');

    import Clicker from './components/clicker.vue'
    import Products from './components/products.vue'
    import Alert from './components/alert.vue'
    import Counter from './components/counter.vue'
    import Todo from './components/todo.vue'

    export default {

        data () {
          return {
              msg: 'hello'
          }
        },

        components: {

          Clicker,
          Products,
          Alert,
          Counter,
          Todo
        }

    }


</script>
