<template>
  <div>
    <HeroSection />
    
    <CampaignSplit />

    <div class="container products-section">
      <h1 class="section-title">Featured Products</h1>
      <div v-if="pending" class="loading">Loading...</div>
      
      <div v-else class="carousel-container">
        
        <button class="nav-btn prev-btn" @click="scroll('left')">&#10094;</button>

        <div class="product-scroller" ref="scrollerRef">
          <ProductCard 
            v-for="item in data?.products" 
            :key="item.id" 
            :product="item" 
            class="scroll-item"
          />
        </div>

        <button class="nav-btn next-btn" @click="scroll('right')">&#10095;</button>

      </div>
    </div>

    <PromoBanner />
    
    <CategorySection />

  </div>
</template>

<script setup>
import { ref } from 'vue';

const { data, pending } = await useFetch('https://dummyjson.com/products?limit=12');

const scrollerRef = ref(null);

const scroll = (direction) => {
  if (scrollerRef.value) {
    const amount = 300;
    scrollerRef.value.scrollBy({
      left: direction === 'left' ? -amount : amount,
      behavior: 'smooth'
    });
  }
};
</script>

<style>
.section-title {
  text-align: center;
  color: #008080;
  margin: 40px 0 30px;
  font-weight: 800;
  text-transform: uppercase;
}

.carousel-container {
  position: relative;
  display: flex;
  align-items: center;
}

.product-scroller {
  display: flex;
  overflow-x: auto;
  gap: 20px;
  padding: 10px 5px;
  scroll-behavior: smooth;
  scrollbar-width: none; 
  -ms-overflow-style: none;
}

.product-scroller::-webkit-scrollbar {
  display: none;
}

.scroll-item {
  min-width: 260px;
  max-width: 260px;
}

.nav-btn {
  position: absolute;
  width: 40px;
  height: 40px;
  background-color: #fff;
  border: 1px solid #ddd;
  color: #333;
  font-size: 1.2rem;
  cursor: pointer;
  z-index: 10;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
  transition: all 0.3s;
}

.nav-btn:hover {
  background-color: #008080;
  color: #fff;
  border-color: #008080;
}

.prev-btn { left: -20px; }
.next-btn { right: -20px; }

@media (max-width: 768px) {
  .nav-btn { display: none; }
  .carousel-container { margin: 0 -20px; padding: 0 20px; }
}
</style>