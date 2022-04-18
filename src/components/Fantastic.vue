<template>
  <div>
    <h1> Fantasy</h1>
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
          name: 'След смерти',
          cost: '$0.99',
          brand: 'Fantacy',
          image: 'https://i1.mybook.io/p/x756/book_covers/67/da/67da7044-7a6d-400e-b4a4-def1dad60774.jpg'
        },
        {
          name: 'Безмолвный пациент',
          cost: '$3.79',
          brand: 'Fantacy',
          image: 'https://i1.mybook.io/p/x756/book_covers/c2/99/c299bff5-9de5-475c-b67d-36996ea6c520.jpg'
        },
        {
          name: 'Под опасным солнцем',
          cost: '$5.99',
          brand: 'Fantacy',
          image: 'https://i1.mybook.io/p/x756/book_covers/7b/8f/7b8f9522-ecf4-4015-aa30-c057c60c6a52.jpg'
        },
        {
          name: 'Код да Винчи',
          cost: '$5.39',
          brand: 'Fantacy',
image: 'https://i3.mybook.io/p/x756/book_covers/52/2b/522b3653-9756-4ac3-a4e5-916692a5feb1.jpg'        },
        {
          name: 'Зов кукушки',
          cost: '$7.99',
          brand: 'Fantacy',
image: 'https://i1.mybook.io/p/x756/book_covers/69/79/69799042-2048-4652-a2be-f92404250e24.jpg'
        },
        {
          name: 'Пассажир',
          cost: '$5.99',
          brand: 'Fantacy',
image: 'https://i2.mybook.io/p/x756/book_covers/ea/a0/eaa0b440-e623-45ed-9b83-837bd5104736.jpg'        },
        {
          name: 'Происхождение',
          cost: '$2.49',
          brand: 'Fantacy',
image: 'https://i3.mybook.io/p/x756/book_covers/5c/18/5c185a8e-9a3c-4726-844f-b8f9f742c410.jpg'
        },
        {
          name: 'Гончие Лилит',
          cost: '$4.59',
          brand: 'Fantacy',
image: 'https://i1.mybook.io/p/x756/book_covers/30/ce/30ce15ab-a782-4229-afa7-1cf9737e3174.jpg'        },
        {
          name: 'Снеговик',
          cost: '$3.39',
          brand: 'Fantacy',
image: 'https://i1.mybook.io/p/x756/book_covers/5f/15/5f155f9c-4b83-418d-9d28-246c690e4e47.jpg'        }
      ]
    }
  },
  methods:{
    addItemToCart(product){
      this.$emit("addItemToCart",product)
    }
  },
  name: "Fantastic.vue"
}
</script>

<style scoped>

</style>
