<template>
  <div>
    <AppHeader />
    
    <div class="container">
      <h1>Featured Products</h1>
      
      <div v-if="pending" class="loading">
        Loading products...
      </div>

      <div v-else class="product-grid">
        <ProductCard 
          v-for="item in data?.products" 
          :key="item.id" 
          :product="item" 
        />
      </div>
    </div>
  </div>
</template>

<script setup>
const { data, pending } = await useFetch('https://dummyjson.com/products')
</script>

<style>
body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #ffffff; 
}

.container {
  padding: 20px;
  max-width: 1200px;
  margin: 0 auto;
}

.loading {
  text-align: center;
  font-size: 1.5rem;
  margin-top: 50px;
  color: #666;
}

.product-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(220px, 1fr)); 
  gap: 40px; 
}
</style>