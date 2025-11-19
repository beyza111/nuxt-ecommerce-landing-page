<template>
  <header class="site-header">
    
    <div class="top-bar">
      <div class="container top-bar-content">
        <div class="top-left">
          <a href="#"><span class="icon">Store</span> Stores</a>
          <a href="#"><span class="icon">Book</span> Catalog</a>
        </div>
        <div class="top-right">
          <span>Call us: (+90) 850 123 45 67</span>
        </div>
      </div>
    </div>

    <div class="main-header">
      <div class="container main-header-content">
        <div class="logo">
          <NuxtLink to="/" class="brand-link">
            <span class="brand-name">watsons</span>
          </NuxtLink>
        </div>

        <div class="search-bar">
          <input type="text" placeholder="Write the product or category you are looking for" />
          <button class="search-btn">🔍</button>
        </div>

        <div class="header-icons">
          <div class="user-info">
            <span>Hello, <strong>Beyza</strong></span>
          </div>
          
          <NuxtLink to="/checkout" class="cart-icon">
            🛒
            <span class="badge">2</span>
          </NuxtLink>
          
        </div>
      </div>
    </div>

    <div class="nav-bar">
      <div class="container">
        <nav>
          <a href="#" class="active">CAMPAIGNS</a>
          <a href="#">PERSONAL CARE</a>
          <a href="#">SKIN CARE</a>
          <a href="#">MAKE - UP</a>
          <a href="#">MOTHER & BABY</a>
          <a href="#">MEN CARE</a>
          <a href="#">HEALTHY LIFE</a>
          <a href="#">BRANDS</a>
        </nav>
      </div>
    </div>

  </header>
</template>

<style scoped>
.site-header {
  font-family: 'Segoe UI', sans-serif;
  background-color: white;
  box-shadow: 0 2px 5px rgba(0,0,0,0.05);
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

.top-bar {
  background-color: #333;
  color: #ccc;
  font-size: 0.75rem;
  padding: 8px 0;
}

.top-bar-content {
  display: flex;
  justify-content: space-between;
}

.top-left a {
  color: #ccc;
  text-decoration: none;
  margin-right: 20px;
  display: inline-flex;
  align-items: center;
  gap: 5px;
}

.top-left a:hover {
  color: white;
}

.main-header {
  padding: 20px 0;
}

.main-header-content {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
}

.brand-link {
  text-decoration: none; 
}

.brand-name {
  font-size: 2rem;
  font-weight: 900;
  color: #008080;
  letter-spacing: -1px;
  text-transform: lowercase;
}

.search-bar {
  flex: 1;
  max-width: 600px;
  display: flex;
  background-color: #f5f5f5;
  border-radius: 20px;
  padding: 5px 15px;
  border: 1px solid #eee;
}

.search-bar input {
  flex: 1;
  border: none;
  background: transparent;
  padding: 10px;
  outline: none;
  font-size: 0.9rem;
}

.search-btn {
  background: none;
  border: none;
  cursor: pointer;
  font-size: 1.2rem;
}

.header-icons {
  display: flex;
  align-items: center;
  gap: 20px;
}

.user-info {
  font-size: 0.9rem;
  color: #555;
}


.cart-icon {
  position: relative;
  font-size: 1.5rem;
  cursor: pointer;
  text-decoration: none; 
  color: inherit; 
  display: flex;
  align-items: center;
}

.badge {
  position: absolute;
  top: -5px;
  right: -10px;
  background-color: #ea4c89;
  color: white;
  font-size: 0.7rem;
  width: 18px;
  height: 18px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
}

.nav-bar {
  border-top: 1px solid #eee;
  padding: 15px 0;
}

.nav-bar nav {
  display: flex;
  justify-content: space-between;
  overflow-x: auto;
}

.nav-bar a {
  text-decoration: none;
  color: #555;
  font-size: 0.85rem;
  font-weight: 600;
  white-space: nowrap;
  padding-bottom: 5px;
  transition: color 0.2s;
}

.nav-bar a:hover, .nav-bar a.active {
  color: #008080;
  border-bottom: 2px solid #008080;
}

@media (max-width: 768px) {
  .main-header-content {
    flex-direction: column;
    gap: 15px;
  }
  
  .search-bar {
    width: 100%;
    order: 3;
  }
  
  .nav-bar nav {
    gap: 20px;
    padding-bottom: 10px;
  }
}
</style>