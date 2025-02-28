<template>
  <div class="card">
    <img :src="product.image" :alt="product.title" />
    <div class="info">
      <h3>{{ product.title }}</h3>
      <p>€ {{ product.price.toFixed(2) }}</p>
    </div>
  </div>
</template>

<script setup>
defineProps(['product']);
</script>

<style scoped>
.card {
  width: 250px;
  /* ✅ Fixed width */
  height: 320px;
  /* ✅ Consistent height */
  backdrop-filter: blur(5px);
  border-radius: 15px;
  padding: 15px;
  text-align: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  cursor: pointer;
  background: rgba(255, 255, 255, 0.9);

  /* ✅ Subtle shadow */
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);
}

/* ✅ Ensure image fills container */
.card img {
  width: 100%;
  height: 180px;
  object-fit: cover;
  /* Fills container */
  border-radius: 15px;
  /* ✅ Rounded corners */
}

/* ✅ Improve hover effect */
.card:hover {
  transform: scale(1.05);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
  /* Slightly stronger shadow */
}

.info {
  margin-top: 10px;
}
</style>
