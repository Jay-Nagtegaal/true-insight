<template>
  <div>

    <section class="reviews" id="reviews">

      <!-- Header -->
      <div class="reviews__header">
        <div class="reviews__label">Ervaringen</div>
        <h2 class="reviews__heading">
          Wat cliënten <em>zeggen</em>
        </h2>
        <p class="reviews__description">
          Ontdek de ervaringen van mensen die de weg naar healing hebben gevonden bij True Insight.
        </p>
      </div>

      <!-- Review cards -->
      <div class="reviews__grid">

        <div class="reviews__card">
          <div class="card__quote-icon">❝</div>
          <div class="card__text">
            "Ik voelde mij door Marion écht gehoord en gezien. Ze neemt de tijd voor je en kijkt
            verder dan oppervlakkige symptoombestrijding. Echt een aanrader!"
          </div>
          <div class="card__stars">
            <span>★</span><span>★</span><span>★</span><span>★</span><span>★</span>
          </div>
          <div class="card__author">
            <div class="card__avatar">A</div>
            <div class="card__author-info">
              <div class="card__author-name">Anna V.</div>
              <div class="card__author-location">Amsterdam</div>
            </div>
          </div>
        </div>

        <div class="reviews__card reviews__card--featured">
          <div class="card__quote-icon">❝</div>
          <div class="card__text">
            "Na jaren van zoeken naar antwoorden, heeft Marion mij eindelijk kunnen helpen de oorzaak
            van mijn klachten te achterhalen. De integrale aanpak werkt."
          </div>
          <div class="card__stars">
            <span>★</span><span>★</span><span>★</span><span>★</span><span>★</span>
          </div>
          <div class="card__author">
            <div class="card__avatar">P</div>
            <div class="card__author-info">
              <div class="card__author-name">Peter K.</div>
              <div class="card__author-location">Amstelveen</div>
            </div>
          </div>
        </div>

        <div class="reviews__card">
          <div class="card__quote-icon">❝</div>
          <div class="card__text">
            "De combinatie van orthomoleculaire therapie en emotiewerk heeft mij enorm geholpen.
            Marion is kundig, warm en professioneel."
          </div>
          <div class="card__stars">
            <span>★</span><span>★</span><span>★</span><span>★</span><span>★</span>
          </div>
          <div class="card__author">
            <div class="card__avatar">L</div>
            <div class="card__author-info">
              <div class="card__author-name">Lisa M.</div>
              <div class="card__author-location">Aalsmeer</div>
            </div>
          </div>
        </div>

      </div>

      <!-- Divider -->
      <div class="reviews__divider"></div>

      <!-- Certifications -->
      <div class="reviews__certs">

        <div class="cert">
          <div class="cert__name">BATC</div>
          <div class="cert__label">Erkend Therapeut</div>
        </div>

        <div class="cert">
          <div class="cert__name">RBCZ</div>
          <div class="cert__label">Geregistreerd</div>
        </div>

        <div class="cert">
          <div class="cert__name">KAB</div>
          <div class="cert__label">Aangesloten</div>
        </div>

        <div class="cert">
          <div class="cert__name">SCAG</div>
          <div class="cert__label">Gecertificeerd</div>
        </div>

      </div>

    </section>

  </div>
</template>

<script>
export default {
  name: 'Reviews'
}
</script>

<style scoped>
/* ── Section wrapper ── */
.reviews {
  background: var(--cream);
  padding: 80px 32px 80px;
}

/* ── Header ── */
.reviews__header {
  text-align: center;
  max-width: 680px;
  margin: 0 auto 56px;
  display: flex;
  flex-direction: column;
  gap: 16px;
}

/* Label */
.reviews__label {
  font-size: 0.72rem;
  font-weight: 600;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--olive);
}

/* Heading */
.reviews__heading {
  font-family: 'Playfair Display', serif;
  font-size: 2.6rem;
  font-weight: 400;
  line-height: 1.25;
  color: var(--text-dark);
  margin: 0;
}

.reviews__heading em {
  font-style: italic;
}

/* Description */
.reviews__description {
  font-size: 0.95rem;
  line-height: 1.75;
  color: var(--text-mid);
  font-weight: 300;
  margin: 0;
}

/* ── Cards grid ── */
.reviews__grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
  max-width: 1100px;
  margin: 0 auto;
  align-items: start;
}

/* ── Single card ── */
.reviews__card {
  background: var(--white);
  border: 1px solid rgba(75, 45, 143, 0.18);
  border-radius: 14px;
  padding: 32px 28px;
  display: flex;
  flex-direction: column;
  gap: 16px;
  transition: box-shadow 0.25s ease, transform 0.25s ease;
}

.reviews__card:hover {
  box-shadow: 0 8px 32px rgba(42, 33, 24, 0.1);
  transform: translateY(-3px);
}

/* Featured (middle) card */
.reviews__card--featured {
  box-shadow: 0 8px 40px rgba(42, 33, 24, 0.12);
}

/* Quote icon */
.card__quote-icon {
  font-size: 2rem;
  line-height: 1;
  color: var(--olive);
  opacity: 0.5;
  font-family: 'Playfair Display', serif;
}

/* Review text */
.card__text {
  font-size: 0.88rem;
  line-height: 1.75;
  color: var(--text-mid);
  font-style: italic;
  font-weight: 300;
}

/* Stars */
.card__stars {
  display: flex;
  gap: 2px;
}

.card__stars span {
  font-size: 0.85rem;
  color: var(--olive);
}

/* Author row */
.card__author {
  display: flex;
  align-items: center;
  gap: 12px;
}

/* Avatar circle */
.card__avatar {
  width: 38px;
  height: 38px;
  border-radius: 50%;
  background: var(--beige);
  color: var(--olive-dark);
  font-size: 0.9rem;
  font-weight: 700;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

/* Author info */
.card__author-info {
  display: flex;
  flex-direction: column;
  gap: 2px;
}

.card__author-name {
  font-size: 0.88rem;
  font-weight: 600;
  color: var(--text-dark);
}

.card__author-location {
  font-size: 0.78rem;
  color: var(--text-mid);
  font-weight: 300;
}

/* ── Divider ── */
.reviews__divider {
  border: none;
  border-top: 1px solid rgba(75, 45, 143, 0.2);
  max-width: 1100px;
  margin: 60px auto 52px;
}

/* ── Certifications ── */
.reviews__certs {
  display: flex;
  justify-content: center;
  gap: 64px;
  max-width: 1100px;
  margin: 0 auto;
}

.cert {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 4px;
}

.cert__name {
  font-family: 'Playfair Display', serif;
  font-size: 1.5rem;
  font-weight: 600;
  color: var(--text-dark);
  letter-spacing: 0.04em;
}

.cert__label {
  font-size: 0.72rem;
  font-weight: 600;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--text-mid);
}
</style>
