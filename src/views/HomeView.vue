<template>
  <div class="home">
    <h1>Onze Producten</h1>
    <div class="grid">
      <ProductCard v-for="product in products" :key="product.id" :product="product" />
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import ProductCard from '@/components/ProductCard.vue';

// const baseURL = import.meta.env.MODE === 'production' ? '/handmades-shop' : '';
// console.log(baseURL);

const products = ref([
  { id: 'p1', title: 'Brillenband (oranje)', price: 5.99, image: `/images/img1.jpg` },
  { id: 'p2', title: 'Brillenband (blauw)', price: 12.99, image: '/images/img2.jpg' }
]);
</script>

<style scoped>
h1 {
  margin-bottom: 20px;
}

.home {
  text-align: center;
  margin-top: 125px;
}

/* ✅ Fixed product width, won't change on resize */
.grid {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: center;
  /* ✅ Center the grid */
  max-width: 1200px;
  margin: 0 auto;
}
</style>
