<template>
    <section class="product-section">
        <h1>Silvia te quiero</h1>
      <div class="product-images">
        <img
          v-for="(image, index) in productImages"
          :key="index"
          :src="image"
          class="product-image"
          @click="openModal(image)"
        />
      </div>
      <div v-if="modalVisible" class="modal" @click="closeModal">
        <img :src="currentImage" />
      </div>
    </section>
  </template>
  
  <script>
  export default {
    data() {
      return {
        productImages: [
          '/images/product1.jpg',
          '/images/product2.jpg',
          '/images/product3.jpg'
        ],
        modalVisible: false,
        currentImage: ''
      };
    },
    methods: {
      openModal(image) {
        this.modalVisible = true;
        this.currentImage = image;
      },
      closeModal() {
        this.modalVisible = false;
      }
    }
  };
  </script>
  
  <style scoped>
  .product-images {
    display: flex;
    justify-content: center;
    gap: 10px;
  }
  
  .product-image {
    width: 100px;
    height: 100px;
    transition: transform 0.3s;
  }
  
  .product-image:hover {
    transform: scale(1.5);
  }
  
  .modal {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background-color: rgba(0, 0, 0, 0.8);
    display: flex;
    justify-content: center;
    align-items: center;
  }
  </style>
  