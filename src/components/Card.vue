<template>
    <div class="container">
      <div class="row">
        <div v-for="(product, index) in products" :key="index" class="col-4">
          <!-- Contenitore del prodotto -->
          <div class="product">
            <!-- Immagine principale -->
            <img :src="product.mainImage" class="main-image" alt="Product">
            <!-- Immagine hover -->
            <img :src="product.hoverImage" class="hover-image" alt="Product">
            <!-- Etichette -->
            <div class="labels">
              <div v-for="(label, index) in product.labels" :key="index" :class="[label.color]">{{ label.text }}</div>
            </div>
            <!-- Icona del cuore -->
            <div class="heart">&#10084;</div>
          </div>
          <!-- Descrizione del prodotto -->
          <div class="description">
            <span class="brand">{{ product.brand }}</span>
            <p><strong>{{ product.description }}</strong></p>
            <span class="price">{{ product.price }}</span> <span class="old-price">{{ product.oldPrice }}</span>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        products: [
          { 
            id: 1, 
            mainImage: 'public/img/1.webp', 
            hoverImage: 'img/2b.webp', // Assumendo che '1b.webp' sia all'interno della cartella 'public'
            labels: [{ text: '-50%', color: 'red' }, { text: 'Sostenibilità', color: 'green' }], 
            brand: "Levi's", 
            description: 'Relaxed fit tee unisex', 
            price: '14.99€', 
            oldPrice: '24.99€' 
          },
          
          
        ]
      }
    }
  }
  </script>
  
  <style scoped lang="scss">
  /* Stili per la griglia */
  .row {
    display: flex;
    flex-wrap: wrap;
    margin: 0 -15px;
  }
  
  .col-4 {
    flex: 0 0 33.333333%;
    max-width: 33.333333%;
    padding: 0 15px;
  }
  
  /* Stili per i prodotti */
  .product {
    position: relative;
    margin-bottom: 20px;
  }
  
  .product img {
    width: 100%;
  }
  
  .labels {
    position: absolute;
    bottom: 20px;
    left: 0;
    display: flex;
  }
  
  .label {
    font-size: 16px;
    font-weight: 700;
    padding: 5px;
    color: white;
    margin-right: 5px;
  }
  
  .red {
    background-color: red;
  }
  
  .green {
    background-color: green;
  }
  
  .heart {
    background-color: white;
    padding: 5px 10px;
    position: absolute;
    top: 20px;
    right: 0;
  }
  </style>
  