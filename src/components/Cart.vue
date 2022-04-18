<template>
  <div>
    <h1> Your Cart</h1>
    <div class="products">
      <div v-for="(product, index) in cart" :key="index">
        <img :src="product.image" />
        <h3>{{product.name}}</h3>
        <div>{{product.cost}}</div>
        <ul><div class="brand">{{product.brand}}</div></ul>
        <button v-on:click="removeItemFromCart(product)">Remove from cart</button>
      </div>
    </div>
    <h2> Subtotal </h2>
  </div>
</template>

<script>
export default {
  props:["cart"],
  methods:{
    removeItemFromCart(product){
      this.$emit("removeItemFromCart",product)
    }
  },
  name: "Cart"
}
</script>

<style scoped>

</style>
