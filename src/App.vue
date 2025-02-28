<template>
  <div>
    <header>
      <img src="/images/handmade-logo.png" alt="Logo" class="logo" />
      <nav>
        <div class="nav-links">
          <router-link to="/">Producten</router-link>
          <router-link to="/contact">Contact</router-link>
        </div>
      </nav>
    </header>

    <router-view />
  </div>
</template>

<style>
header > img {
  margin-left: 10vw;
}

header > nav {
  margin-right: 10vw;
}

body {
  margin: 0;
  padding: 0;
  font-family: Arial, sans-serif;
}

nav {
  position: fixed;
  top: 15px;
  right: 40px;
  /* Move it to the right */
  display: flex;
  gap: 20px;
  background: rgba(255, 255, 255, 0.5);
  backdrop-filter: blur(10px);
  padding: 10px 20px;
  border-radius: 10px;
}

.logo {
  width: 100px;
  height: 100px;
  position: absolute;
  top: 10px;
  left: 30px;
  z-index: 100;
}

.nav-links {
  display: flex;
  gap: 20px;
}

.nav-links a {
  text-decoration: none;
  font-size: 18px;
  font-weight: bold;
  position: relative;
  padding: 8px 14px;
  transition: 0.3s ease;
  border-radius: 8px;
  border: 1px solid transparent;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
}

.nav-links a:hover {
  background-color: rgba(201, 201, 201, 0.4);
}

.nav-links a.router-link-active {
  color: #e9e9e9;
  background-color: #007bff;
  border: 1px solid #007bff;
  font-weight: bold;
}

@media (max-width: 768px) {
  header > img {
    margin-left: 0px;
  }

  header > nav {
    margin-right: 0px;
  }
}
</style>
