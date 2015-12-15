<template>
  <div class="container">
  <div :class="AlertClasses" v-show="show">
  <slot></slot>
  <span class-"close-btn" @click="close()">X</span>
  </div>
  </div>
</template>

<style lang="sass">
  .alert{
    width: 200px;
    padding: 10px;
    background: #ddd;
    position: relative;


  }

  .close-btn{
    position: absolute;
    top: 0;
    right: 0;
  }

  .error{
    background: $maroon;
  }

  .success{
    background: green;
  }
</style>

<script>


  export default {

    props: ['type'],

    data () {
    return {
      show: true
    }
    },

  computed: {
    AlertClasses () {
      return {
        'alert': true,
        'error': this.type === 'error',
        'success': this.type === 'success',
        'gal-6': true
      }
    }
  },
  methods: {

    close () {
      this.show = !this.show;
      console.log(this.show);
    }

  }

  }
</script>
