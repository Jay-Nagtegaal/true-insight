<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import { useRouter } from 'vue-router'

const router = useRouter()
const navRef = ref(null)

// ── Section colour map ──
const sectionStyles = {
  home:        { bg: '#F5F4FF', border: 'rgba(75,45,143,0.25)', text: '#1A1464' },
  about:       { bg: '#FFFFFF', border: 'rgba(75,45,143,0.15)', text: '#1A1464' },
  methodieken: { bg: '#F5F4FF', border: 'rgba(75,45,143,0.25)', text: '#1A1464' },
  diensten:    { bg: '#FFFFFF', border: 'rgba(75,45,143,0.15)', text: '#1A1464' },
  reviews:     { bg: '#F5F4FF', border: 'rgba(75,45,143,0.25)', text: '#1A1464' },
}

let observer = null

function applyStyle(id) {
  const style = sectionStyles[id] || sectionStyles.home
  if (navRef.value) {
    navRef.value.style.background    = style.bg
    navRef.value.style.borderColor   = style.border
    navRef.value.style.color         = style.text
  }
}

function initObserver() {
  const sections = ['about', 'methodieken', 'diensten', 'reviews']
  const elements = sections
    .map(id => document.getElementById(id))
    .filter(Boolean)

  observer = new IntersectionObserver(
    (entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          applyStyle(entry.target.id)
        }
      })
      // If nothing is intersecting we're at the top (home)
      const anyVisible = entries.some(e => e.isIntersecting)
      if (!anyVisible && window.scrollY < 200) {
        applyStyle('home')
      }
    },
    { threshold: 0.25 }
  )

  elements.forEach(el => observer.observe(el))
}

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

function goToDiensten() {
  document.getElementById('diensten')?.scrollIntoView({ behavior: 'smooth' })
}

function goToReviews() {
  document.getElementById('reviews')?.scrollIntoView({ behavior: 'smooth' })
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
  // Wait a tick for sections to be rendered
  setTimeout(initObserver, 100)
})

onUnmounted(() => {
  window.removeEventListener('scroll', onScroll)
  cancelAnimationFrame(animFrameId)
  observer?.disconnect()
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
        <button class="button" @click="goToDiensten">Diensten</button>
        <button class="button" @click="goToReviews">Reviews</button>
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
  background: var(--cream);
  border-bottom: 1px solid rgba(75, 45, 143, 0.25);
  padding-left: 50px;
  padding-right: 50px;
  box-sizing: border-box;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  z-index: 1000;
  will-change: transform;
  font-family: 'Lato', sans-serif;
  transition: background 0.5s ease, border-color 0.5s ease;
}

.personal-information {
  display: flex;
  flex-direction: row;
  gap: 20px;
  font-size: 11px;
  font-weight: 300;
  color: var(--text-mid);
  letter-spacing: 0.02em;
}

.title h1 {
  margin-bottom: 2px;
  margin-left: -5px;
  cursor: pointer;
  font-family: 'Playfair Display', serif;
  font-size: 1.3rem;
  font-weight: 700;
  color: var(--text-dark);
}

.title {
  font-size: 0.72rem;
  font-weight: 300;
  color: var(--text-mid);
  letter-spacing: 0.06em;
  text-transform: uppercase;
}

.nav-bar-buttons {
  display: flex;
  align-items: center;
  margin-right: -12px;
  gap: 2px;
}

.nav-bar-left {
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 4px;
}

.nav-bar-right {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-end;
  gap: 4px;
}

.region-information {
  font-size: 11px;
  font-weight: 300;
  color: var(--text-mid);
  display: flex;
  justify-content: flex-end;
  letter-spacing: 0.02em;
}

#make-appointment {
  background: var(--olive) !important;
  color: var(--white) !important;
  border-radius: 2px;
  font-weight: 600;
  letter-spacing: 0.08em;
  padding-left: 20px;
  padding-right: 20px;
}

#make-appointment:hover {
  background: var(--olive-dark) !important;
}

.button {
  border: 0;
  background: transparent;
  color: var(--text-dark);
  height: 50px;
  padding-left: 12px;
  padding-right: 12px;
  font-family: 'Lato', sans-serif;
  font-size: 0.82rem;
  font-weight: 400;
  letter-spacing: 0.04em;
  cursor: pointer;
  transition: color 0.2s ease, background 0.2s ease;
  border-radius: 2px;
}

.button:hover {
  color: var(--olive);
  background: rgba(75, 45, 143, 0.08);
}
</style>