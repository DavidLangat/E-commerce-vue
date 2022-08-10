<template>
   <h2>OnSale</h2>
   <ProductItem
  v-for="product in products"
  :key="product.id"
  :product="product"
  @add-to-cart="$emit('add-to-cart', $event)"
  class="products__item"
/>
   <button
  class="product__btn"
  @click="addToCart"
>
  Quick add
   <img class="onsale" src="./img/onsale1.jpg" alt="" onclick="clickme">
   </button>
      <img class="onsale" src="./img/onsale2.jpg" alt="">
   <img class="onsale" src="./img/onsale3.jpg" alt="">
   <img class="onsale" src="./img/onsale4.jpg" alt="">
   <img class="onsale" src="./img/onsale5.jpg" alt="">
   <img class="onsale" src="./img/onsale6.jpg" alt="">
</template>
<script>

export default {
  name: 'OnSale',
  props: {
    msg: String
  },
  methods: {
    addToCart() {
      this.$emit('add-to-cart', this.product.id, 1);
    }
}
}
</script>
<style scoped>
.onsale{
    margin-right: 3%;
    margin-bottom: 3%;
    width: 29%;
    border-radius: 10px;
    border: 2px solid black;
}
.onsale:hover{
        width: 25%;
        border-radius: 50px;
        border:5px solid rgb(13, 13, 88);

}
</style>
