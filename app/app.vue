<template>
  <div>
    <AppHeader />
    
    <HeroSection />
    
    <CampaignSplit />
    
    <div class="container">
      <h1 class="section-title">Featured Products</h1>
      <div v-if="pending" class="loading">Loading...</div>
      <div v-else class="product-grid">
        <ProductCard 
          v-for="item in data?.products" 
          :key="item.id" 
          :product="item" 
        />
      </div>
    </div>

    <PromoBanner />
    
    <CategorySection />

    <AppFooter />

  </div>
</template>

<script setup>
const { data, pending } = await useFetch('https://dummyjson.com/products?limit=8') 
</script>

<style>

body {
  font-family: 'Segoe UI', sans-serif;
  margin: 0;
  padding: 0;
  background-color: #fff;
}
.container {
  padding: 20px;
  max-width: 1200px;
  margin: 0 auto;
}
.section-title {
  text-align: center;
  color: #4aa1a8;
  margin: 40px 0;
}
.product-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(220px, 1fr)); 
  gap: 40px;
}
</style>