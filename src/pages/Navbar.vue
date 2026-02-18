<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import { useRouter } from 'vue-router'

const router = useRouter()
const navRef = ref(null)

function goHome() {
  router.push('/')
  window.scrollTo({ top: 0, behavior: 'smooth' })
}

function goToAbout() {
  document.getElementById('about')?.scrollIntoView({ behavior: 'smooth' })
}

function goToMethodieken() {
  document.getElementById('methodieken')?.scrollIntoView({ behavior: 'smooth' })
}

let lastScrollY = 0
let targetOffset = 0
let currentOffset = 0
let animFrameId = null

const lerp = (a, b, t) => a + (b - a) * t

function animate() {
  // Smoothly move currentOffset toward targetOffset
  currentOffset = lerp(currentOffset, targetOffset, 0.18)
  // Slowly decay target back to 0 (spring back)
  targetOffset = lerp(targetOffset, 0, 0.14)

  if (navRef.value) {
    navRef.value.style.transform = `translateY(${currentOffset.toFixed(2)}px)`
  }

  animFrameId = requestAnimationFrame(animate)
}

function onScroll() {
  const scrollY = window.scrollY
  const delta = scrollY - lastScrollY
  // Shift target by a fraction of scroll delta, clamped so nav never leaves screen
  targetOffset = Math.max(-28, Math.min(0, targetOffset - delta * 0.45))
  lastScrollY = scrollY
}

onMounted(() => {
  lastScrollY = window.scrollY
  window.addEventListener('scroll', onScroll, { passive: true })
  animFrameId = requestAnimationFrame(animate)
})

onUnmounted(() => {
  window.removeEventListener('scroll', onScroll)
  cancelAnimationFrame(animFrameId)
})
</script>

<template>
  <div class="nav-bar" ref="navRef">
    <div class="nav-bar-left">
      <div class="personal-information">
        <div class="phone-number">+31 6 1234 5678</div>
        <div class="email">marion.gulpers@trueinsight.nl</div>
      </div>
      <div class="title">
        <h1 @click="router.push('/')">True Insight</h1>
        Integrale Geneeskunde
      </div>
    </div>
    <div class="nav-bar-right">
      <div class="region-information">
        <p>Regio Amsterdam - Amstelveen - Aalsmeer</p>
      </div>
      <div class="nav-bar-buttons">
        <button class="button" @click="goHome">Home</button>
        <button class="button" @click="goToAbout">Over Mij</button>
        <button class="button" @click="goToMethodieken">Methodieken</button>
        <button class="button">Diensten</button>
        <button class="button">Reviews</button>
        <button class="button">Contact</button>
        <button class="button" id="make-appointment">Maak Afspraak</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
.nav-bar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100px;
  background: white;
  border-bottom: black solid 1px;
  border-top: black solid 1px;
  padding-left: 50px;
  padding-right: 50px;
  box-sizing: border-box;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  z-index: 1000;
  will-change: transform;
}

.personal-information {
  display:  flex;
  flex-direction: row;
  gap: 20px;
  font-size: 12px;
}

.title h1{
  margin-bottom: 2px;
  margin-left: -5px;
  cursor: pointer;
}

.nav-bar-buttons {
  display: flex;
  align-items: center;
  margin-left: auto;
  margin-right: -20px;
}

.nav-bar-right {
  display: flex;
  flex-direction: column;
}
.region-information {
  font-size: 12px;
  display: flex;
  justify-content: flex-end;
}

#make-appointment {
  padding-left: 20px;
  padding-right: 20px;
}

.button {
  border: 0;
  background: white;
  color: black;
  height: 50px;
  padding-left: 10px;
  padding-right: 10px;
}

.button:hover {
  background: #135adf;
  cursor: pointer;
  color: white;
}
</style>