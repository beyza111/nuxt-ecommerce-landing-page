<template>
  <section class="hero-wrapper">
    
    <div class="hero-image-container">
      <img 
        src="https://images.unsplash.com/photo-1512909006721-3d6018887383?auto=format&fit=crop&w=1920&q=80" 
        alt="Holiday Beauty Collection" 
        class="hero-bg"
      />
    </div>

    <div class="container content-layer">
      <div class="white-card">
        <h2 class="brand-title">Watsons Collection</h2>
        <p class="campaign-text">
          Discover the Advent Calendar with<br>
          <strong>24 beauty surprises!</strong>
        </p>
        <button class="discover-btn">DISCOVER</button>
      </div>
    </div>

  </section>
</template>

<style scoped>
.hero-wrapper {
  position: relative;
  width: 100%;
  height: 500px;
  overflow: hidden;
  display: flex;
  align-items: center;
  background-color: #fceef2;
}

.hero-image-container {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
}

.hero-bg {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
}

.content-layer {
  position: relative;
  z-index: 2;
  width: 100%;
  display: flex;
  justify-content: flex-end;
  padding-right: 50px;
}

.white-card {
  background-color: white;
  padding: 40px 50px;
  border-radius: 12px;
  max-width: 480px;
  text-align: center;
  box-shadow: 0 15px 35px rgba(0,0,0,0.15); 
}

.brand-title {
  font-size: 2rem;
  font-weight: 800;
  margin: 0 0 15px;
  color: #000;
  letter-spacing: -0.5px;
}

.campaign-text {
  font-size: 1.1rem;
  color: #333;
  margin-bottom: 30px;
  line-height: 1.6;
}

.discover-btn {
  background-color: white;
  color: #000;
  border: 2px solid #000;
  padding: 15px 60px;
  font-size: 1rem;
  font-weight: 800;
  cursor: pointer;
  border-radius: 8px;
  transition: all 0.3s ease;
  letter-spacing: 1px;
  text-transform: uppercase;
  width: 100%;
}

.discover-btn:hover {
  background-color: #000;
  color: white;
}

@media (max-width: 768px) {
  .hero-wrapper {
    height: auto;
    flex-direction: column;
  }
  
  .hero-image-container {
    position: relative;
    height: 300px;
  }
  
  .content-layer {
    justify-content: center;
    padding: 20px;
    background-color: #fceef2;
  }
  
  .white-card {
    width: 100%;
    max-width: 100%;
    box-shadow: none;
    padding: 30px 20px;
  }
}
</style>