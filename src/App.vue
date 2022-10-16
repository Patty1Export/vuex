<template>
  <div id="app">
      <!--First Step, Create a component in the App.vue-->
      <!--To passed the data, use v-bind in each of the components-->
      <product-list-one v-bind:products="products"></product-list-one>
      <product-list-two v-bind:products="products"></product-list-two>
  </div>
</template>

<script>
//After creating ids in the components, import both components
import ProductListOne from './components/ProductListOne.vue';
import ProductListTwo from './components/ProductListTwo.vue';

export default {
  //Lastly, register both of the components
  components: {
    'product-list-one': ProductListOne,
    'product-list-two': ProductListTwo,
  },
  name: 'app',
  data () {
    return {
      // Second step, put products as attribute with an array of data
      // Third step, create a components folder in the src folder with its new files
      // Create two files which is ProductListOne.vue and ProductListTwo.vue
        products: [
          {name:'Banana Skin', price: 20 }, //these are the objects
          {name:'Shiny Star', price: 40 },
          {name:'Green Shells', price: 60 },
          {name:'Red Shells', price: 80 },
        ],
    }
  }
}
</script>

<style scoped>
body{
  font-family: Ubuntu;
  color: #555;
}
</style>
