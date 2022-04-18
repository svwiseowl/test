<template>
  <div>
    <h1> Top of the week</h1>
    <div class="products">
      <div v-for="(product, index) in products" :key="index">
        <img :src="product.image" />
        <h3>{{product.name}}</h3>
        <button v-on:click="addItemToCart(product)">Add to cart</button>
        <div class="cost">{{product.cost}}</div>
      </div>
    </div>
  </div>

</template>

<script>
export default {
  data: () =>{
    return{
      products :[
        {
          name: 'Клара и Тень',
          cost: '$0.99',
         image: 'https://i2.mybook.io/p/x756/book_covers/b6/e9/b6e9b0e2-a88e-4970-9280-c29befcb2349.jpg'        },
        {
          name: 'Стекло',
          cost: '$5.99',
          image:'https://i1.mybook.io/p/x756/book_covers/26/59/26595518-c51b-4177-8a00-9478042771ca.jpg' },
      {
          name: 'Рагнарёк',
          cost: '$5.99',
          image: 'https://i2.mybook.io/p/x756/book_covers/30/00/300043ba-0dc7-4a59-b7e1-f1e2ae00a2a7.jpg' }     ]
    }
  },
  methods:{
addItemToCart(product){
  this.$emit("addItemToCart",product)
    }
  },
  name: "Products.vue"
}
</script>

<style >
.products .image{
 width: 10px;
  height: 10px;
}
</style>
