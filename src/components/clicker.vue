<template>
<div class="container">
    <a @click="counter()">component a! click me</a>
    <p>Clicked: {{count}}</p>
    </div>
</template>




<style lang="sass">
    template {
        font-family: sans-serif;
    }
    a{
        background-color: aqua;
        color: white;
        padding: 10px;
        font-family: sans-serif;
    }
</style>

<script>
    export default {

        data () {
            return {

                count: 0
            }
        },

        methods: {

        counter () {

        this.count++;
    }
    }

    }
</script>
