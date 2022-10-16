<template>
  <div id="product-list-one"> <!--Create id for ProductListOne.vue which is product-list-one-->
    <h2>Product List One</h2>
    <ul>
      <!--loop data using v-for with products-->
      <li v-for="product in products">
          <span class="name">{{product.name}}</span> <!--output product name-->
          <span class="price">{{product.price}}</span> <!--output product price-->
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  //accept the data in the binds in the root components, used props
  props: ['products'],//display the bind array products
  data () {
    return {

    }
  }
}
</script>
<!--Style for product list one -->
<style scoped>
#product-list-one{
  background: #FFF8B1;
  box-shadow: 1px 2px 3px rgba(0,0,0,0.2);
  margin-bottom: 30px;
  padding: 10px 20px;
}
#product-list-one ul{
  padding: 0;
}
#product-list-one li{
  display: inline-block;
  margin-right: 10px;
  margin-top: 10px;
  padding: 20px;
  background: rgba(255,255,255,0.7);
}
.price{
  font-weight: bold;
  color: #E8800C;
}

</style>
