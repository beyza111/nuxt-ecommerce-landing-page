<template>
  <section class="split-campaigns">
    <div class="container grid-layout">
      
      <div class="campaign-card left-card">
        <div class="badge-app">APP EXCLUSIVE</div>
        <div class="card-content">
          <div class="text-part">
            <h3 class="card-title">GIFT WEEK</h3>
            <p class="card-desc">
              Free Gift with all<br>
              <strong>L'Oreal Professional</strong> purchases!
            </p>
            <button class="action-btn">DISCOVER</button>
            <p class="tiny-text">*Valid until 18 Nov 2025. Limited to 250 stocks.</p>
          </div>
          <div class="img-part">
            <img src="https://images.unsplash.com/photo-1626784215021-2e39ccf971cd?auto=format&fit=crop&w=300&q=80" alt="Loreal Products" />
          </div>
        </div>
      </div>

      <div class="campaign-card right-card">
        <div class="card-content">
          <div class="text-part">
            <h3 class="card-title">Special Sets</h3>
            <p class="card-desc">
              Discover the perfume sets<br>
              <strong>selected just for you!</strong>
            </p>
            <button class="action-btn outline">DISCOVER</button>
          </div>
          <div class="img-part">
            <img src="https://images.unsplash.com/photo-1541643600914-78b084683601?auto=format&fit=crop&w=300&q=80" alt="Perfume Sets" />
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<style scoped>
.split-campaigns {
  padding: 30px 0;
  background-color: #fff;
}

.grid-layout {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 30px;
}

.campaign-card {
  border-radius: 8px;
  overflow: hidden;
  position: relative;
  height: 280px;
  display: flex;
  align-items: center;
  padding: 0 40px;
}

.left-card {
  background-color: #e8e2d2; 
}

.right-card {
  background-color: #fae6e0;
}

.card-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}

.text-part {
  flex: 1;
  z-index: 2;
}

.img-part img {
  height: 220px;
  width: auto;
  object-fit: contain;
  mix-blend-mode: multiply;
}

.badge-app {
  position: absolute;
  top: 20px;
  left: 0;
  background-color: #000;
  color: #fff;
  font-size: 0.7rem;
  font-weight: bold;
  padding: 5px 10px;
  border-top-right-radius: 4px;
  border-bottom-right-radius: 4px;
}

.card-title {
  font-size: 1.4rem;
  font-weight: 800;
  margin-bottom: 10px;
  color: #000;
  text-transform: uppercase;
}

.card-desc {
  font-size: 0.95rem;
  color: #333;
  margin-bottom: 20px;
  line-height: 1.4;
}

.tiny-text {
  font-size: 0.65rem;
  color: #666;
  margin-top: 10px;
}

.action-btn {
  background-color: #000;
  color: #fff;
  border: 1px solid #000;
  padding: 10px 30px;
  font-weight: bold;
  font-size: 0.8rem;
  cursor: pointer;
  border-radius: 4px;
  text-transform: uppercase;
}

.action-btn.outline {
  background-color: transparent;
  color: #000;
}

.action-btn:hover {
  transform: scale(1.05);
  transition: transform 0.2s;
}

@media (max-width: 768px) {
  .grid-layout {
    grid-template-columns: 1fr;
  }
  
  .campaign-card {
    height: auto;
    padding: 30px;
    flex-direction: column-reverse;
    text-align: center;
  }
  
  .card-content {
    flex-direction: column-reverse;
    gap: 20px;
  }

  .img-part img {
    height: 150px;
  }
}
</style>