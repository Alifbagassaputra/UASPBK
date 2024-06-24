<template>
  <div id="app">
    <Navbar />
    <div class="content">
      <router-view />
    </div>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';

export default {
  name: 'App',
  components: {
    Navbar,
  },
};
</script>

<style scoped>
#app {
  font-family: Arial, sans-serif;
  text-align: center;
}

.content {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  margin-top: -60px;
}
</style>
