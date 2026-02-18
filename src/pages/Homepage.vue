<template>
  <div class="homepage">
    <Navbar />
    <Home />
    <AboutMe />
    <Methodieken />
    <Diensten />
    <Reviews />
  </div>
</template>

<script>
import Navbar from './Navbar.vue'
import Home from './Home.vue'
import AboutMe from './AboutMe.vue'
import Methodieken from './Methodieken.vue'
import Diensten from './Diensten.vue'
import Reviews from './Reviews.vue'

export default {
  name: 'Homepage',
  components: { Navbar, Home, AboutMe, Methodieken, Diensten, Reviews }
}
</script>

<style scoped>
.homepage {
  display: flex;
  flex-direction: column;
  background: var(--cream);
  width: 100%;
  min-height: 100vh;
  color: var(--text-dark);
}
</style>

