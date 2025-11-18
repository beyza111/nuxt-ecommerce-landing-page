<template>
  <div class="card">
    <div class="image-container">
      <img :src="product.thumbnail" :alt="product.title" class="card-image" />
    </div>
    
    <div class="card-details">
      <div class="price">${{ product.price }}</div>
      <h3 class="card-title">{{ product.title }}</h3>
      <p class="card-brand">{{ product.brand || product.category }}</p>
      <button class="add-btn">Add to Cart</button>
    </div>
  </div>
</template>

<script setup>
defineProps(['product']);
</script>

<style scoped>
.card {
  border-radius: 0;
  overflow: hidden;
  transition: all 0.3s;
  background: white;
  display: flex;
  flex-direction: column;
  padding: 10px;
  border: 1px solid transparent;
}

.card:hover {
  border-color: #e0e0e0;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

.image-container {
  width: 100%;
  height: 250px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 10px;
  background-color: #fff;
}

.card-image {
  max-width: 100%;
  max-height: 100%; 
  object-fit: contain;
}

.card-details {
  gap: 5px;
  display: flex;
  flex-direction: column;
  text-align: left;
}

.card-title {
  font-size: 0.95rem;
  font-weight: 400;
  margin: 0;
  color: #333;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

.price {
  font-weight: 700;
  font-size: 1.1rem;
  color: #000;
}

.card-brand {
  font-size: 0.8rem;
  color: #888;
  margin: 0;
  text-transform: uppercase;
}

.add-btn {
  margin-top: 10px;
  background-color: #333; 
  color: white;
  border: none;
  padding: 10px;
  width: 100%;
  font-size: 0.85rem;
  cursor: pointer;
  text-transform: uppercase;
  letter-spacing: 1px;
  transition: background 0.2s;
}

.add-btn:hover {
  background-color: #000; 
}
</style>
