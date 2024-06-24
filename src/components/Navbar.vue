<template>
  <nav class="navbar">
    <div class="navbar-brand">
      <router-link to="/" class="navbar-item">WEATHER</router-link>
    </div>
    <div class="task-links">
      <div class="dropdown" @click="toggleDropdown">
        <div class="navbar-item">TUGAS UAS ALIF ▼</div>
        <div class="dropdown-menu" :class="{ 'is-active': isDropdownActive }">
          <a href="https://alif-projetc-cv.web.app/" class="navbar-item" target="_blank">TUGAS 1</a>
          <a href="https://tugas2alifbagassaputra.vercel.app/" class="navbar-item" target="_blank">TUGAS 2</a>
          <a href="https://alifbagassaputratugas3.vercel.app/" class="navbar-item" target="_blank">TUGAS 3</a>
          <a href="https://alifbagastugas4leb.vercel.app/" class="navbar-item" target="_blank">TUGAS 4</a>
          <a href="https://alifstorepage.vercel.app/" class="navbar-item" target="_blank">TUGAS 5</a>
          <a href="https://tugas6alif.vercel.app/" class="navbar-item" target="_blank">TUGAS 6</a>
          <a href="https://tugas7alif.vercel.app/" class="navbar-item" target="_blank">TUGAS 7</a>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
  data() {
    return {
      isDropdownActive: false
    };
  },
  methods: {
    toggleDropdown() {
      this.isDropdownActive = !this.isDropdownActive;
    }
  }
};
</script>

<style scoped>
.navbar {
  background-color: #0d0f11d4;
  color: #fff;
  padding: 10px 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.navbar-brand {
  display: flex;
  align-items: center;
}

.navbar-item {
  color: #fff;
  text-decoration: none;
  margin: 0 10px;
  padding: 10px;
  border-radius: 5px;
  transition: background-color 0.3s, color 0.3s;
  font-size: 18px;
}

.navbar-item:hover {
  background-color: #1177e4;
}

.task-links {
  display: flex;
  align-items: center;
}

.dropdown {
  position: relative;
  cursor: pointer;
}

.dropdown-menu {
  display: none;
  position: absolute;
  top: calc(100% + 10px);
  left: 50%;
  transform: translateX(-50%);
  background-color: #1b1e1d;
  border-radius: 10px;
  padding: 10px 0;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
  z-index: 1000;
  width: 200px;
  opacity: 0;
  pointer-events: none;
  transition: opacity 0.3s ease;
}

.dropdown-menu.is-active {
  display: block;
  opacity: 1;
  pointer-events: auto;
}

.dropdown-menu .navbar-item {
  display: block;
  width: 100%;
  padding: 10px 20px;
  font-size: 16px;
}

.dropdown-menu .navbar-item:hover {
  background-color: #0056b3;
}

.navbar-item.active {
  background-color: #0056b3;
}
</style>
