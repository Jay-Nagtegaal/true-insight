<template>
  <footer class="footer">

    <div class="footer__main">

      <!-- Left: Brand column -->
      <div class="footer__brand">
        <div class="footer__logo">
          <span class="footer__logo-icon">🌿</span>
          <span class="footer__logo-name">True Insight</span>
        </div>
        <p class="footer__tagline">
          Complementaire Holistische Praktijk voor Integrale Geneeskunde.
          Streven naar inzicht in de oorzaken van klachten sinds 2002.
        </p>
      </div>

      <!-- Middle: Navigation column -->
      <div class="footer__nav">
        <div class="footer__col-heading">Navigatie</div>
        <ul class="footer__links">
          <li><a href="#" class="footer__link" @click.prevent="scrollTo('top')">Home</a></li>
          <li><a href="#" class="footer__link" @click.prevent="scrollTo('about')">Over Mij</a></li>
          <li><a href="#" class="footer__link" @click.prevent="scrollTo('methodieken')">Methodieken</a></li>
          <li><a href="#" class="footer__link" @click.prevent="scrollTo('diensten')">Diensten</a></li>
          <li><a href="#" class="footer__link" @click.prevent="scrollTo('contact')">Contact</a></li>
        </ul>
      </div>

      <!-- Right: Contact column -->
      <div class="footer__contact">
        <div class="footer__col-heading">Contact</div>
        <div class="footer__contact-items">
          <a href="mailto:marion.gulpers@trueinsight.nl" class="footer__link">
            marion.gulpers@trueinsight.nl
          </a>
          <a href="tel:+31612345678" class="footer__link">+31 6 1234 5678</a>
          <div class="footer__address">
            <span>Regio Amsterdam</span>
            <span>Amstelveen – Aalsmeer</span>
          </div>
        </div>
      </div>

    </div>

    <!-- Bottom bar -->
    <div class="footer__bottom">
      <div class="footer__divider"></div>
      <div class="footer__bottom-row">
        <div class="footer__copyright">
          © 2024 True Insight. Alle rechten voorbehouden.
        </div>
        <div class="footer__made-with">
          Gemaakt met ♡ voor holistische healing
        </div>
      </div>
    </div>

  </footer>
</template>

<script>
export default {
  name: 'Footer',
  methods: {
    scrollTo(target) {
      if (target === 'top') {
        window.scrollTo({ top: 0, behavior: 'smooth' })
      } else {
        document.getElementById(target)?.scrollIntoView({ behavior: 'smooth' })
      }
    }
  }
}
</script>

<style scoped>
/* ── Footer wrapper ── */
.footer {
  background: var(--white);
  padding: 64px 32px 0;
}

/* ── Main row ── */
.footer__main {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr;
  gap: 64px;
  max-width: 1100px;
  margin: 0 auto;
  padding-bottom: 48px;
}

/* ── Brand column ── */
.footer__brand {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

/* Logo */
.footer__logo {
  display: flex;
  align-items: center;
  gap: 8px;
}

.footer__logo-icon {
  font-size: 1.2rem;
}

.footer__logo-name {
  font-family: 'Playfair Display', serif;
  font-size: 1.3rem;
  font-weight: 700;
  color: var(--text-dark);
}

/* Tagline */
.footer__tagline {
  font-size: 0.88rem;
  line-height: 1.75;
  color: var(--text-mid);
  font-weight: 300;
  max-width: 340px;
  margin: 0;
}

/* ── Column heading ── */
.footer__col-heading {
  font-size: 0.95rem;
  font-weight: 700;
  color: var(--text-dark);
  margin-bottom: 18px;
}

/* ── Navigation column ── */
.footer__nav {
  display: flex;
  flex-direction: column;
}

.footer__links {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.footer__link {
  font-size: 0.88rem;
  color: var(--olive);
  text-decoration: none;
  font-weight: 300;
  transition: color 0.2s;
  cursor: pointer;
}

.footer__link:hover {
  color: var(--olive-dark);
}

/* ── Contact column ── */
.footer__contact {
  display: flex;
  flex-direction: column;
}

.footer__contact-items {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.footer__address {
  display: flex;
  flex-direction: column;
  gap: 2px;
  font-size: 0.88rem;
  color: var(--text-mid);
  font-weight: 300;
}

/* ── Bottom bar ── */
.footer__bottom {
  max-width: 1100px;
  margin: 0 auto;
  padding-bottom: 36px;
}

.footer__divider {
  border: none;
  border-top: 1px solid rgba(75, 45, 143, 0.2);
  margin-bottom: 24px;
}

.footer__bottom-row {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.footer__copyright {
  font-size: 0.8rem;
  color: var(--text-mid);
  font-weight: 300;
}

.footer__made-with {
  font-size: 0.8rem;
  color: var(--text-mid);
  font-weight: 300;
}
</style>
