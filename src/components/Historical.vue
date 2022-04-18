<template>
  <div>
    <h1>Historical books</h1>
    <div class="products">
      <div v-for="(product, index) in products" :key="index">
        <img :src="product.image" />
        <h3>{{product.name}}</h3>
        <div class="cost">{{product.cost}}</div>
        <ul><div class="brand">{{product.brand}}</div></ul>
        <button v-on:click="addItemToCart(product)">Add to cart</button>

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
          name: '1984',
          cost: '$0.99',
          brand: 'Historical',
image: 'https://i3.mybook.io/p/x756/book_covers/32/a8/32a8032e-60cb-4a14-95b2-a145a3048426.jpg'        },
        {
          name: 'Таинственная история Билли Миллигана',
          cost: '$5.99',
          brand: 'Historical',
image: 'https://i2.mybook.io/p/x756/book_covers/a4/95/a4956176-0c9a-43c3-a4ef-520aa8e7c756.jpg'
        },
        {
          name: 'Таинственный остров',
          cost: '$5.99',
          brand: 'Historical',
image: 'https://i3.mybook.io/p/x756/book_covers/a8/6a/a86afb0b-7d83-4a25-b035-7d4708424c92.jpg'        },
        {
          name: 'Азазель',
          cost: '$5.99',
          brand: 'Historical',
image: 'https://i1.mybook.io/p/x756/book_covers/60/a2/60a2c5fb-5570-4e01-8435-3e6434b366e3.jpg'        },
        {
          name: 'На Западном фронте без перемен',
          cost: '$5.99',
          brand: 'Historical',
image: 'https://i2.mybook.io/p/x756/book_covers/00/4c/004cbac3-5661-4f4c-a6fd-ee144d59023c.jpg'        },
        {
          name: 'Семь смертей Эвелины Хардкасл',
          cost: '$5.99',
          brand: 'Historical',
image: 'https://i1.mybook.io/p/x756/book_covers/21/d4/21d416d8-23c6-4228-8d85-6f280124eac5.jpg'        },
        {
          name: 'Империя должна умереть',
          cost: '$5.99',
          brand: 'Historical',
image: 'https://i1.mybook.io/p/x756/book_covers/2f/60/2f601159-863a-48ce-a574-90c29ddce119.jpg'        },
        {
          name: 'Cookies',
          cost: '$5.99',
          brand: 'Historical',
image: 'https://i1.mybook.io/p/x756/book_covers/cd/ef/cdef8ebc-d20f-4fd1-8464-95a77d6e8954.jpg'        },
        {
          name: 'Дверь в Лето',
          cost: '$5.99',
          brand: 'Historical',
image: 'https://i1.mybook.io/p/x756/book_covers/76/c0/76c05af3-a111-4716-aaea-2936131b756a.jpg'        }
      ]
    }
  },
  methods:{
    addItemToCart(product){
      this.$emit("addItemToCart",product)
    }
  },
  name: "Historical.vue"
}
</script>

<style scoped>

</style>
