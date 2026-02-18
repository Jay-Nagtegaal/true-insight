<template>
  <div class="homepage">
    <Navbar />

    <section class="hero">

      <!-- LEFT: Text column -->
        <div class="hero__text">

        <div class="hero__badge">
          <span class="badge__icon">♡</span>
          <span class="badge__label">Officieel erkend BATC Therapeut</span>
        </div>

        <h1 class="hero__heading">
          Streven naar <em>inzicht</em> in oorzaken
        </h1>

        <p class="hero__description">
          True Insight is een complementaire holistische praktijk voor integrale
          geneeskunde. Wij helpen je de kernoorzaken van je klachten te
          achterhalen en je eigen zelfhelend vermogen te activeren.
        </p>

        <div class="hero__buttons">
          <a href="#" class="btn btn--text">Plan een Consult &rarr;</a>
          <a href="#" class="btn btn--outline">Meer Informatie</a>
        </div>

        <hr class="hero__divider" />

        <div class="hero__stats">
          <div class="stat">
            <span class="stat__number">20+</span>
            <span class="stat__label">Jaar Ervaring</span>
          </div>
          <div class="stat">
            <span class="stat__number">1000+</span>
            <span class="stat__label">Cliënten</span>
          </div>
          <div class="stat">
            <span class="stat__number">BATC</span>
            <span class="stat__label">Gecertificeerd</span>
          </div>
        </div>

      </div>

      <!-- RIGHT: Image column -->
      <div class="hero__image-wrapper">
        <img
          class="hero__image"
          src="https://images.unsplash.com/photo-1506126613408-eca07ce68773?w=800&auto=format&fit=crop"
          alt="Meditatie bij zonsondergang"
        />

        <div class="hero__quote-card">
          <p class="quote__text">
            "Het is niet de tijd die heeft maar de oprechte toewijding waarmee
            je wezenlijke aandacht aan jezelf besteed."
          </p>
          <p class="quote__author">— Marion Gulpers</p>
        </div>
      </div>

    </section>
  </div>
</template>

<script>
import Navbar from "./Navbar.vue";

export default {
  name: 'Homepage',
  components: { Navbar }
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
  height: 2000px;
  font-family: 'Calibri', 'Segoe UI', sans-serif;
  color: #1a1a1a;
}

/* ── Hero section ── */
.hero {
  display: flex;
  align-items: center;
  gap: 64px;
  max-width: 1100px;
  margin: 0 auto;
  padding: 140px 32px 80px;
}

/* ── Left: Text column ── */
.hero__text {
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 24px;
}

/* Badge */
.hero__badge {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  font-size: 0.85rem;
  color: #555;
}

.badge__icon {
  color: #c0392b;
  font-size: 1rem;
}

/* Heading */
.hero__heading {
  font-size: 2.8rem;
  font-weight: 700;
  line-height: 1.2;
  margin: 0;
  color: #111;
}

.hero__heading em {
  font-style: italic;
  font-weight: 700;
}

/* Description */
.hero__description {
  font-size: 1rem;
  line-height: 1.7;
  color: #444;
  max-width: 480px;
  margin: 0;
}

/* Buttons */
.hero__buttons {
  display: flex;
  align-items: center;
  gap: 20px;
}

.btn {
  text-decoration: none;
  font-size: 0.95rem;
  cursor: pointer;
  transition: opacity 0.2s;
}

.btn--text {
  color: #1a1a1a;
  font-weight: 500;
  border: none;
  background: none;
  padding: 0;
}

.btn--text:hover {
  opacity: 0.6;
}

.btn--outline {
  border: 1.5px solid #1a1a1a;
  color: #1a1a1a;
  background: transparent;
  padding: 10px 22px;
  border-radius: 4px;
  font-weight: 400;
}

.btn--outline:hover {
  background: #f5f5f5;
}

/* Divider */
.hero__divider {
  border: none;
  border-top: 1px solid #ddd;
  margin: 0;
}

/* Stats */
.hero__stats {
  display: flex;
  gap: 40px;
}

.stat {
  display: flex;
  flex-direction: column;
  gap: 2px;
}

.stat__number {
  font-size: 1.5rem;
  font-weight: 700;
  color: #111;
}

.stat__label {
  font-size: 0.78rem;
  color: #777;
  text-transform: uppercase;
  letter-spacing: 0.04em;
}

/* ── Right: Image column ── */
.hero__image-wrapper {
  flex: 1;
  position: relative;
  max-width: 480px;
}

.hero__image {
  width: 100%;
  height: 480px;
  object-fit: cover;
  border-radius: 16px;
  display: block;
}

/* Quote card overlay */
.hero__quote-card {
  position: absolute;
  bottom: 24px;
  left: -24px;
  background: rgba(255, 255, 255, 0.92);
  backdrop-filter: blur(6px);
  border-radius: 10px;
  padding: 18px 22px;
  max-width: 280px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
}

.quote__text {
  font-size: 0.82rem;
  line-height: 1.6;
  color: #333;
  margin: 0 0 8px 0;
}

.quote__author {
  font-size: 0.82rem;
  font-weight: 600;
  color: #111;
  margin: 0;
}
</style>

