<template>
  <div>

    <section class="diensten" id="diensten">

      <!-- Header -->
      <div class="diensten__header">
        <div class="diensten__label">Diensten</div>
        <h2 class="diensten__heading">
          Ontdek onze <em>behandelingen</em>
        </h2>
        <p class="diensten__description">
          Bij True Insight werken we altijd integraal en gericht op de oorzaken van je klachten,
          niet alleen de symptomen.
        </p>
      </div>

      <!-- Cards -->
      <div class="diensten__grid">

        <!-- Card 1 -->
        <div class="diensten__card">
          <div class="card__top">
            <div class="card__icon">🛡️</div>
            <div class="card__badge">Populair</div>
          </div>
          <div class="card__category">Preventie &amp; Inzicht</div>
          <div class="card__title">Integrale Health Check</div>
          <div class="card__description">
            Een uitgebreide gezondheidscheck die kijkt naar alle aspecten van je welzijn:
            fysiek, mentaal en emotioneel.
          </div>
          <ul class="card__list">
            <li class="card__list-item">Levend bloed analyse</li>
            <li class="card__list-item">Bioresonantie scan</li>
            <li class="card__list-item">Uitgebreide anamnese</li>
            <li class="card__list-item">Leefstijl analyse</li>
            <li class="card__list-item">Persoonlijk adviesrapport</li>
          </ul>
          <a href="#" class="card__link">Meer Informatie &rarr;</a>
        </div>

        <!-- Card 2 (highlighted) -->
        <div class="diensten__card diensten__card--featured">
          <div class="card__top">
            <div class="card__icon">✨</div>
          </div>
          <div class="card__category">Integrale Begeleiding</div>
          <div class="card__title">Holistische Sessie</div>
          <div class="card__description">
            Persoonlijke behandelsessies gericht op het achterhalen en verwerken van de
            kernoorzaken van je klachten.
          </div>
          <ul class="card__list">
            <li class="card__list-item">Emotie therapie</li>
            <li class="card__list-item">Trauma verwerking</li>
            <li class="card__list-item">Energetische healing</li>
            <li class="card__list-item">Voedingsadvies</li>
            <li class="card__list-item">Follow-up begeleiding</li>
          </ul>
          <a href="#" class="card__link">Meer Informatie &rarr;</a>
        </div>

        <!-- Card 3 -->
        <div class="diensten__card">
          <div class="card__top">
            <div class="card__icon">🕐</div>
          </div>
          <div class="card__category">Voortgang &amp; Ondersteuning</div>
          <div class="card__title">Vervolgconsult</div>
          <div class="card__description">
            Regelmatige consulten om je voortgang te monitoren en behandelingen bij te sturen
            waar nodig.
          </div>
          <ul class="card__list">
            <li class="card__list-item">Voortgangsbespreking</li>
            <li class="card__list-item">Aanpassing behandelplan</li>
            <li class="card__list-item">Verdiepende therapie</li>
            <li class="card__list-item">Praktische tips</li>
            <li class="card__list-item">Blijvende ondersteuning</li>
          </ul>
          <a href="#" class="card__link">Meer Informatie &rarr;</a>
        </div>

      </div>

    </section>

    <!-- Wave transition into next section -->
    <div class="diensten__wave-bottom">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 90" preserveAspectRatio="none">
        <path d="M0,40 C240,90 480,0 720,50 C960,100 1200,10 1440,40 L1440,90 L0,90 Z" fill="var(--cream)"/>
      </svg>
    </div>

  </div>
</template>

<script>
export default {
  name: 'Diensten'
}
</script>

<style scoped>
/* ── Section wrapper ── */
.diensten {
  background: var(--white);
  padding: 80px 32px 60px;
}

/* ── Header ── */
.diensten__header {
  text-align: center;
  max-width: 700px;
  margin: 0 auto 56px;
  display: flex;
  flex-direction: column;
  gap: 16px;
}

/* Label */
.diensten__label {
  font-size: 0.72rem;
  font-weight: 600;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--olive);
}

/* Heading */
.diensten__heading {
  font-family: 'Playfair Display', serif;
  font-size: 2.6rem;
  font-weight: 400;
  line-height: 1.25;
  color: var(--text-dark);
  margin: 0;
}

.diensten__heading em {
  font-style: italic;
}

/* Description */
.diensten__description {
  font-size: 0.95rem;
  line-height: 1.75;
  color: var(--text-mid);
  font-weight: 300;
  margin: 0;
}

/* ── Cards grid ── */
.diensten__grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
  max-width: 1100px;
  margin: 0 auto;
  align-items: start;
}

/* ── Single card ── */
.diensten__card {
  background: var(--white);
  border: 1px solid rgba(124, 107, 78, 0.18);
  border-radius: 14px;
  padding: 32px 28px 24px;
  display: flex;
  flex-direction: column;
  gap: 14px;
  transition: box-shadow 0.25s ease, transform 0.25s ease;
}

.diensten__card:hover {
  box-shadow: 0 8px 32px rgba(42, 33, 24, 0.1);
  transform: translateY(-3px);
}

/* Featured (middle) card */
.diensten__card--featured {
  box-shadow: 0 8px 40px rgba(42, 33, 24, 0.12);
}

/* Top row: icon + optional badge */
.card__top {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
}

/* Icon */
.card__icon {
  font-size: 1.3rem;
  line-height: 1;
}

/* "Populair" badge */
.card__badge {
  font-size: 0.7rem;
  font-weight: 600;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--olive);
  border: 1px solid var(--olive);
  border-radius: 20px;
  padding: 3px 10px;
}

/* Category */
.card__category {
  font-size: 0.75rem;
  font-weight: 600;
  letter-spacing: 0.06em;
  color: var(--olive);
  text-transform: uppercase;
}

/* Title */
.card__title {
  font-family: 'Playfair Display', serif;
  font-size: 1.45rem;
  font-weight: 600;
  color: var(--text-dark);
  line-height: 1.3;
}

/* Description */
.card__description {
  font-size: 0.85rem;
  line-height: 1.7;
  color: var(--text-mid);
  font-weight: 300;
}

/* Checklist */
.card__list {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 8px;
  margin: 0;
  padding: 0;
}

.card__list-item {
  font-size: 0.84rem;
  color: var(--text-mid);
  font-weight: 300;
  display: flex;
  align-items: center;
  gap: 10px;
}

.card__list-item::before {
  content: '✓';
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 18px;
  height: 18px;
  border: 1.5px solid var(--olive);
  border-radius: 50%;
  font-size: 0.65rem;
  color: var(--olive);
  flex-shrink: 0;
  font-weight: 700;
}

/* "Meer Informatie" link */
.card__link {
  display: inline-block;
  margin-top: 8px;
  font-size: 0.82rem;
  font-weight: 600;
  color: var(--text-dark);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  padding-bottom: 1px;
  transition: color 0.2s, border-color 0.2s;
  text-align: center;
}

.card__link:hover {
  color: var(--olive);
  border-color: var(--olive);
}

/* ── Wave divider ── */
.diensten__wave-bottom {
  width: 100%;
  line-height: 0;
  background: var(--white);
}

.diensten__wave-bottom svg {
  display: block;
  width: 100%;
  height: 90px;
}
</style>
