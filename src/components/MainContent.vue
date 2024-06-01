<template>
    <main>
      <div class="container">
        <div class="row">
          <Card 
            v-for="card in cards" 
            :key="card.id" 
            :mainImage="card.mainImage" 
            :hoverImage="card.hoverImage" 
            :labels="card.labels" 
            :brand="card.brand" 
            :description="card.description" 
            :price="card.price" 
            :oldPrice="card.oldPrice" 
          />
        </div>
      </div>
    </main>
  </template>
  
  <script>
  import Card from './Card.vue'
  
  export default {
    name: 'MainContent',
    components: {
      Card
    },
    data() {
      return {
        cards: [
          { id: 1, mainImage: 'public/img/1.webp', hoverImage: 'public/img/1b.webp', labels: [{ text: '-50%', color: 'red' }, { text: 'Sostenibilità', color: 'green' }], brand: "Levi's", description: 'Relaxed fit tee unisex', price: '14.99€', oldPrice: '24.99€' },
          { id: 2, mainImage: 'public/img/2.webp', hoverImage: 'public/img/2b.webp', labels: [{ text: '-50%', color: 'red' }], brand: 'Guess', description: 'ROSES TEE', price: '20.99€', oldPrice: '29.99€' },
          { id: 3, mainImage: 'public/img/3.webp', hoverImage: 'public/img/3b.webp', labels: [{ text: '-30%', color: 'red' }], brand: 'Come Zucchero Filato', description: 'VOGLIA DI COLORI PASTELLO', price: '129.99€', oldPrice: '184.99€' },
          { id: 4, mainImage: 'public/img/4.webp', hoverImage: 'public/img/4b.webp', labels: [{ text: '-50%', color: 'red' }, { text: 'Sostenibilità', color: 'green' }], brand: "Levi's", description: 'tee unisex', price: '14.99€', oldPrice: '29.99€' },
          { id: 5, mainImage: 'public/img/5.webp', hoverImage: 'public/img/5b.webp', labels: [], brand: 'Maya Deluxe', description: 'Stripe bodice', price: '99.99€', oldPrice: '' },
          { id: 6, mainImage: 'public/img/6.webp', hoverImage: 'public/img/6b.webp', labels: [{ text: 'Sostenibilità', color: 'green' }], brand: 'Esprit', description: 'maglione - black', price: '29.99€', oldPrice: '' }
        ]
      }
    }
  }
  </script>
  