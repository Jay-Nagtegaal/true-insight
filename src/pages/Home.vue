<template>
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
          "Het is niet de tijd die heelt maar de oprechte toewijding waarmee
          je wezenlijke aandacht aan jezelf besteed."
        </p>
        <p class="quote__author">— Marion Gulpers</p>
      </div>
    </div>

  </section>

  <!-- Wave transition to next section -->
  <div class="hero__wave">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 90" preserveAspectRatio="none">
      <path d="M0,40 C240,90 480,0 720,50 C960,100 1200,10 1440,40 L1440,90 L0,90 Z" fill="#ffffff"/>
    </svg>
  </div>
</template>

<script>
export default {
  name: 'Home'
}
</script>

<style scoped>
/* ── Hero section ── */
.hero {
  display: flex;
  align-items: center;
  gap: 64px;
  max-width: 1100px;
  margin: 0 auto;
  padding: 140px 32px 100px;
}

/* ── Left: Text column ── */
.hero__text {
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 28px;
}

/* Badge */
.hero__badge {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  font-size: 0.78rem;
  font-weight: 600;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--olive);
}

.badge__icon {
  color: var(--olive);
  font-size: 0.9rem;
}

/* Heading */
.hero__heading {
  font-family: 'Playfair Display', serif;
  font-size: 3rem;
  font-weight: 400;
  line-height: 1.25;
  margin: 0;
  color: var(--text-dark);
}

.hero__heading em {
  font-style: italic;
  font-weight: 400;
}

/* Description */
.hero__description {
  font-size: 0.98rem;
  line-height: 1.8;
  color: var(--text-mid);
  max-width: 460px;
  margin: 0;
  font-weight: 300;
}

/* Buttons */
.hero__buttons {
  display: flex;
  align-items: center;
  gap: 24px;
}

.btn {
  text-decoration: none;
  font-size: 0.75rem;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  cursor: pointer;
  transition: all 0.25s ease;
}

.btn--text {
  color: var(--text-dark);
  border: none;
  background: none;
  padding: 0;
  border-bottom: 1px solid var(--text-dark);
  padding-bottom: 2px;
}

.btn--text:hover {
  color: var(--olive);
  border-color: var(--olive);
}

.btn--outline {
  border: 1.5px solid var(--olive);
  color: var(--white);
  background: var(--olive);
  padding: 12px 28px;
  border-radius: 2px;
}

.btn--outline:hover {
  background: var(--olive-dark);
  border-color: var(--olive-dark);
}

/* Divider */
.hero__divider {
  border: none;
  border-top: 1px solid var(--beige);
  margin: 0;
}

/* Stats */
.hero__stats {
  display: flex;
  gap: 48px;
}

.stat {
  display: flex;
  flex-direction: column;
  gap: 4px;
}

.stat__number {
  font-family: 'Playfair Display', serif;
  font-size: 1.6rem;
  font-weight: 600;
  color: var(--text-dark);
}

.stat__label {
  font-size: 0.72rem;
  color: var(--text-mid);
  text-transform: uppercase;
  letter-spacing: 0.08em;
  font-weight: 600;
}

/* ── Right: Image column ── */
.hero__image-wrapper {
  flex: 1;
  position: relative;
  max-width: 480px;
}

.hero__image {
  width: 100%;
  height: 500px;
  object-fit: cover;
  border-radius: 12px;
  display: block;
}

/* Quote card overlay */
.hero__quote-card {
  position: absolute;
  bottom: 28px;
  left: -28px;
  background: var(--cream);
  border-radius: 8px;
  padding: 20px 24px;
  max-width: 290px;
  box-shadow: 0 8px 32px rgba(42, 33, 24, 0.12);
}

.quote__text {
  font-family: 'Playfair Display', serif;
  font-size: 0.85rem;
  font-style: italic;
  line-height: 1.7;
  color: var(--text-dark);
  margin: 0 0 10px 0;
}

.quote__author {
  font-size: 0.78rem;
  font-weight: 600;
  letter-spacing: 0.06em;
  color: var(--olive);
  margin: 0;
}
/* Wave divider */
.hero__wave {
  width: 100%;
  line-height: 0;
  margin-top: -2px;
}

.hero__wave svg {
  display: block;
  width: 100%;
  height: 90px;
}
</style>