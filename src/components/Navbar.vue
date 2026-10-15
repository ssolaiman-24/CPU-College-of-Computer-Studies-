<template>
  <header class="navbar-header">
    <nav class="navbar">
      <div class="logo-container">
        <RouterLink to="/#hero">
          <img src="/images/cpu_ccs.png" alt="CCS Logo" class="logo-img" />
          <span class="logo-text">CPU-CCS</span>
        </RouterLink>
      </div>
      <ul class="nav-links">
        <li><RouterLink to="/#hero">Home</RouterLink></li>
        <li><RouterLink to="/#programs">Programs</RouterLink></li>
        <li><RouterLink to="/#faculty">Faculty & Staff</RouterLink></li>
        <li><RouterLink to="/#partnerships">Partnerships</RouterLink></li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
.navbar-header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: #002244; 
  border-bottom: 2px solid rgba(255, 255, 255, 0.1);
  color: white;
  z-index: 1000;
}
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1280px;
  margin: 0 auto;
  padding: 0.6rem 2rem;
}
.logo-container a {
  display: flex;
  align-items: center;
  gap: 10px;
  text-decoration: none;
  color: white;
  font-weight: 700;
  font-size: 1.1rem;
}
.logo-img {
  width: 36px;
  height: 36px;
  object-fit: contain;
  border-radius: 4px;
}
.nav-links {
  display: flex;
  list-style: none;
  gap: 1.8rem;
  margin: 0;
  padding: 0;
}
.nav-links a {
  color: #cbd5e1;
  text-decoration: none;
  font-weight: 500;
  font-size: 0.9rem;
  transition: color 0.3s ease;
}
.nav-links a:hover, .nav-links a.router-link-exact-active {
  color: #ff9f0a;
}

@media (max-width: 768px) {
  .nav-links {
    gap: 0.8rem;
    font-size: 0.75rem;
  }
}
</style>

