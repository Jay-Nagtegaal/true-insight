<template>
  <div>

    <!-- Wave transition from white (AboutMe) into cream (Methodieken) -->
    <div class="methodieken__wave-top">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 90" preserveAspectRatio="none">
        <path d="M0,40 C240,90 480,0 720,50 C960,100 1200,10 1440,40 L1440,0 L0,0 Z" fill="#ffffff"/>
      </svg>
    </div>

    <section class="methodieken" id="methodieken">

      <!-- Header -->
      <div class="methodieken__header">
        <div class="methodieken__label">Methodieken</div>
        <h2 class="methodieken__heading">
          Diverse disciplines voor <em>complete healing</em>
        </h2>
        <p class="methodieken__description">
          Marion Gulpers is opgeleid in meerdere, elkaar aanvullende disciplines om je integraal en
          optimaal te kunnen begeleiden tijdens je zoektocht naar genezing.
        </p>
      </div>

      <!-- Cards grid -->
      <div class="methodieken__grid">

        <div class="methodieken__card">
          <div class="card__icon">🔬</div>
          <div class="card__title">Levend Bloed Analyse</div>
          <div class="card__description">
            Microscopische analyse met donkerveld en fase contrast microscoop voor diepgaand inzicht.
          </div>
        </div>

        <div class="methodieken__card">
          <div class="card__icon">🍎</div>
          <div class="card__title">Orthomoleculaire Adviezen</div>
          <div class="card__description">
            Epigenetische voedings- en supplementadviezen, onafhankelijk en zonder verkoop.
          </div>
        </div>

        <div class="methodieken__card">
          <div class="card__icon">〰️</div>
          <div class="card__title">Bioresonantie</div>
          <div class="card__description">
            MWO-Multiwave Oscillator, Rife Phanotron Plasma lamp en Qest4/Asyra analyse.
          </div>
        </div>

        <div class="methodieken__card">
          <div class="card__icon">🧠</div>
          <div class="card__title">Emotie Therapie</div>
          <div class="card__description">
            The Journey, Mindfulness, Holistische EMDR, Hypnotherapie, EFT en TAT.
          </div>
        </div>

        <div class="methodieken__card">
          <div class="card__icon">✨</div>
          <div class="card__title">Energetische Healing</div>
          <div class="card__description">
            Reiki, Soul & Chakra healing, Reconnective Healing en Soulretrieval.
          </div>
        </div>

        <div class="methodieken__card">
          <div class="card__icon">🤝</div>
          <div class="card__title">Geweldloze Communicatie</div>
          <div class="card__description">
            Communicatie volgens Marshall Rosenberg als basis voor alle interacties.
          </div>
        </div>

        <div class="methodieken__card">
          <div class="card__icon">🌿</div>
          <div class="card__title">Detox & Ontgifting</div>
          <div class="card__description">
            Ontzuring en ontslakking voor een schoon en vitaal lichaam.
          </div>
        </div>

        <div class="methodieken__card">
          <div class="card__icon">⚡</div>
          <div class="card__title">Voetreflexologie</div>
          <div class="card__description">
            Stimulatie van reflexzones voor balans en welzijn in het hele lichaam.
          </div>
        </div>

      </div>

    </section>

    <!-- Wave transition from cream (Methodieken) into next white section -->
    <div class="methodieken__wave-bottom">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 90" preserveAspectRatio="none">
        <path d="M0,40 C240,90 480,0 720,50 C960,100 1200,10 1440,40 L1440,90 L0,90 Z" fill="#ffffff"/>
      </svg>
    </div>

  </div>
</template>

<script>
export default {
  name: 'Methodieken'
}
</script>

<style scoped>
/* ── Wave dividers ── */
.methodieken__wave-top,
.methodieken__wave-bottom {
  width: 100%;
  line-height: 0;
  background: var(--cream);
}

.methodieken__wave-top svg,
.methodieken__wave-bottom svg {
  display: block;
  width: 100%;
  height: 90px;
}

/* ── Section wrapper ── */
.methodieken {
  background: var(--cream);
  padding: 60px 32px 80px;
}

/* ── Header ── */
.methodieken__header {
  text-align: center;
  max-width: 700px;
  margin: 0 auto 56px;
  display: flex;
  flex-direction: column;
  gap: 16px;
}

/* Label */
.methodieken__label {
  font-size: 0.72rem;
  font-weight: 600;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--olive);
}

/* Heading */
.methodieken__heading {
  font-family: 'Playfair Display', serif;
  font-size: 2.6rem;
  font-weight: 400;
  line-height: 1.25;
  color: var(--text-dark);
  margin: 0;
}

.methodieken__heading em {
  font-style: italic;
}

/* Description */
.methodieken__description {
  font-size: 0.95rem;
  line-height: 1.75;
  color: var(--text-mid);
  font-weight: 300;
  margin: 0;
}

/* ── Cards grid ── */
.methodieken__grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
  max-width: 1100px;
  margin: 0 auto;
}

/* ── Single card ── */
.methodieken__card {
  background: var(--white);
  border: 1px solid rgba(124, 107, 78, 0.18);
  border-radius: 12px;
  padding: 28px 24px;
  display: flex;
  flex-direction: column;
  gap: 12px;
  transition: box-shadow 0.25s ease, transform 0.25s ease;
}

.methodieken__card:hover {
  box-shadow: 0 8px 28px rgba(42, 33, 24, 0.1);
  transform: translateY(-3px);
}

/* Icon */
.card__icon {
  font-size: 1.4rem;
  line-height: 1;
}

/* Title */
.card__title {
  font-size: 0.95rem;
  font-weight: 700;
  color: var(--text-dark);
  line-height: 1.3;
}

/* Description */
.card__description {
  font-size: 0.82rem;
  line-height: 1.65;
  color: var(--text-mid);
  font-weight: 300;
}
</style>
