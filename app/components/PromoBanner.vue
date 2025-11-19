<template>
  <section class="promo-container">
    <div class="container promo-content">
      <div class="promo-text">
        <span class="small-tag">YOUR FAVORITES PRODUCTS</span>
        
        <h2>ONE CLICK AWAY<br>FROM YOUR HOMES!</h2>
        
        <div class="discount-box">
          <span class="huge-text">60%</span>
          <div class="discount-label">
            <span>DISCOUNT</span>
            <span class="tiny-note">ON SELECTED ITEMS</span>
          </div>
        </div>

        <button class="shop-btn">SHOP NOW</button>
      </div>
      
      <img src="https://shopping.tallink.com/_next/image?url=http%3A%2F%2Fwwtll018.fleet.zone%3A28152%2Fimages%2Fprod%2F2%2FA%2F8%2F8%2F2A88F427-413F-4878-A222-E347553F1D61_1_big.png&w=3840&q=80" alt="Promo Products" class="promo-img">
    </div>
  </section>
</template>

<style scoped>
.promo-container {
  background-color: #8FD3D3; 
  margin: 40px 0;
  padding: 0;
  overflow: hidden;
  display: flex;
  align-items: center;
  min-height: 400px;
}

.promo-content {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
}

.promo-text {
  color: #1a4f6d; 
  flex: 1;
  padding: 40px;
  z-index: 2;

  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 15px; 
}

.small-tag {
  font-size: 0.85rem;
  font-weight: 700;
  letter-spacing: 2px;
  opacity: 0.7;
  text-transform: uppercase;
}

h2 {
  font-size: 2.8rem; 
  margin: 0;
  line-height: 1.1;
  font-weight: 900; 
  text-transform: uppercase;
}


.discount-box {
  display: flex;
  align-items: center;
  gap: 15px;
  margin: 10px 0;
  padding: 10px 0;
  border-top: 2px solid rgba(26, 79, 109, 0.2);
  border-bottom: 2px solid rgba(26, 79, 109, 0.2);
  width: fit-content;
}

.huge-text {
  font-size: 3.5rem;
  font-weight: 900;
  line-height: 1;
}

.discount-label {
  display: flex;
  flex-direction: column;
  line-height: 1.2;
}

.discount-label span:first-child {
  font-size: 1.5rem;
  font-weight: 800;
}

.tiny-note {
  font-size: 0.7rem;
  font-weight: 600;
  opacity: 0.8;
}

.shop-btn {
  background-color: #1a4f6d;
  color: white;
  padding: 15px 40px;
  border: none;
  font-weight: 800;
  cursor: pointer;
  border-radius: 0px;
  font-size: 1rem;
  transition: all 0.3s;
  width: fit-content; 
  letter-spacing: 1px;
}

.shop-btn:hover {
  background-color: #0f3a52;
  transform: translateY(-2px);
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}

.promo-img {
  max-height: 450px;
  width: auto;
  object-fit: contain;
  filter: drop-shadow(-10px 10px 20px rgba(0,0,0,0.1)); 
  margin-right: -30px; 
}

@media (max-width: 768px) {
  .promo-container {
    padding: 40px 0;
    text-align: center;
  }

  .promo-content {
    flex-direction: column;
  }

  .promo-text {
    padding: 20px;
    align-items: center; 
  }
  
  .discount-box {
    justify-content: center;
    width: 100%;
  }

  h2 {
    font-size: 2rem;
  }

  .promo-img {
    margin-right: 0;
    margin-top: 20px;
    max-height: 250px;
    max-width: 90%;
  }
}
</style>