<template>
  <div class="homepage">
    <Navbar />
    <Home />
    <AboutMe />
  </div>
</template>

<script>
import Navbar from './Navbar.vue'
import Home from './Home.vue'
import AboutMe from './AboutMe.vue'

export default {
  name: 'Homepage',
  components: { Navbar, Home, AboutMe }
}
</script>

<style scoped>
/* ── Page wrapper ── */
.homepage {
  display: flex;
  flex-direction: column;
  background: #ffffff;
  width: 100%;
  min-height: 100vh;
  font-family: 'Calibri', 'Segoe UI', sans-serif;
  color: #1a1a1a;
}
</style>

