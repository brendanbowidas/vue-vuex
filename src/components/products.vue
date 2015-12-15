<template>
    <div class="container">
        <select v-model="selected">
            <option v-for="product in products" :value="{product: product}">{{product.name}}</option>
        </select><br/>

        <ul>
            <li v-for="retailer in selected.product.retailers">{{retailer.name}}</li>
        </ul>
    </div>
</template>


<style lang="sass">
    ul {
        list-style-type: none

    }
</style>


<script>
    export default {


        data () {
          return {
              products: [],
              selected: ''
          }
        },

        ready () {

            this.$http.get('http://homestead.app/api/product?include=retailers', (data, status, request) => {
                this.$set('products', data)

            }).error((data, status, request) => {
                console.log(status);
            });
        },
        methods: {
            getSelected () {
                console.log(this.selected);
            }
        }
    }


</script>
