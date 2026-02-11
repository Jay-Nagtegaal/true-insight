<template>
  <div class="homepage">
    <Navbar />
    <
  </div>
</template>

<script>
import Navbar from "./Navbar.vue";

export default {
  name: 'Homepage',
  components: {Navbar}
}
</script>

<style scoped>
.homepage {
  display: flex;
  flex-direction: column;
  align-items: center;
  background: blue;
  width: 100%;
  height: 1000px;
  font-family: "Roboto", sans-serif
}
</style>

