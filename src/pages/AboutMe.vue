<template>
  <section class="about" id="about">

    <!-- LEFT: Image column -->
    <div class="about__image-wrapper">
      <img
        class="about__image"
        src="https://images.unsplash.com/photo-1559839734-2b71ea197ec2?w=600&auto=format&fit=crop"
        alt="Marion Gulpers"
      />
      <div class="about__stat">
        <span class="about__stat-number">22</span>
        <span class="about__stat-label">Jaar Ervaring</span>
      </div>
    </div>

    <!-- RIGHT: Text column -->
    <div class="about__text">

      <div class="about__label">Over True Insight</div>

      <h2 class="about__heading">
        Levenskunst van deze <em>moderne tijd</em>
      </h2>

      <div class="about__paragraphs">
        <p class="about__paragraph">
          Marion Gulpers, orthomoleculair therapeut en evolutiepsycholoog, leeft en werkt
          volgens een moderne levensfilosofie: je kunt zelf je leven, je gezondheid en je
          geluk beïnvloeden.
        </p>
        <p class="about__paragraph">
          Door aandacht te geven aan de oorzaken en deze daadwerkelijk te verwerken, verander je
          je gevoelsleven op een positieve manier. Door inzicht in wie je bent en de verwerking van
          blokkades tot in de kern, geef je jezelf de mogelijkheid te functioneren zoals je werkelijk
          bent.
        </p>
      </div>

      <div class="about__features">

        <div class="about__feature">
          <span class="feature__icon">♡</span>
          <div class="feature__content">
            <p class="feature__title">Holistische Benadering</p>
            <p class="feature__description">
              Werken op fysiek, mentaal, emotioneel én energetisch niveau voor complete healing.
            </p>
          </div>
        </div>

        <div class="about__feature">
          <span class="feature__icon">📖</span>
          <div class="feature__content">
            <p class="feature__title">Orthomoleculaire Therapie</p>
            <p class="feature__description">
              Wetenschappelijk onderbouwde voedings- en supplementadvies afgestemd op jouw lichaam.
            </p>
          </div>
        </div>

        <div class="about__feature">
          <span class="feature__icon">👥</span>
          <div class="feature__content">
            <p class="feature__title">Persoonlijke Begeleiding</p>
            <p class="feature__description">
              Individuele aandacht en maatwerk behandelingen voor jouw specifieke situatie.
            </p>
          </div>
        </div>

        <div class="about__feature">
          <span class="feature__icon">🏆</span>
          <div class="feature__content">
            <p class="feature__title">Erkende Kwaliteit</p>
            <p class="feature__description">
              BATC gecertificeerd met meer dan 20 jaar ervaring in complementaire geneeskunde.
            </p>
          </div>
        </div>

      </div>
    </div>

  </section>
</template>

<script>
export default {
  name: 'AboutMe'
}
</script>

<style scoped>
/* ── About section ── */
.about {
  position: relative;
  display: flex;
  align-items: center;
  gap: 64px;
  width: 100vw;
  margin-left: calc(50% - 50vw);
  padding: 80px max(32px, calc(50vw - 550px)) 80px;
  background: var(--white);
  overflow: hidden;
}

/* 'Welcome' watermark */
.about::after {
  content: 'Welcome';
  position: absolute;
  top: 50%;
  left: -2%;
  transform: translateY(-50%);
  font-family: 'Playfair Display', serif;
  font-size: clamp(80px, 14vw, 200px);
  font-weight: 700;
  color: rgba(42, 33, 24, 0.04);
  white-space: nowrap;
  pointer-events: none;
  letter-spacing: -0.02em;
  line-height: 1;
}

/* Keep content above pseudo-elements */
.about__image-wrapper,
.about__text {
  position: relative;
  z-index: 1;
}

/* ── Left: Image column ── */
.about__image-wrapper {
  flex: 1;
  max-width: 420px;
}

.about__image {
  width: 100%;
  height: 500px;
  object-fit: cover;
  border-radius: 12px;
  display: block;
}

/* Stat overlay */
.about__stat {
  position: absolute;
  top: 50%;
  right: -28px;
  transform: translateY(-50%);
  background: var(--cream);
  border-radius: 8px;
  padding: 20px 26px;
  box-shadow: 0 8px 32px rgba(42, 33, 24, 0.1);
  display: flex;
  flex-direction: column;
  align-items: center;
}

.about__stat-number {
  font-family: 'Playfair Display', serif;
  font-size: 2.2rem;
  font-weight: 600;
  color: var(--text-dark);
  line-height: 1;
}

.about__stat-label {
  font-size: 0.72rem;
  font-weight: 600;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--olive);
  margin-top: 6px;
}

/* ── Right: Text column ── */
.about__text {
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

/* Label */
.about__label {
  font-size: 0.72rem;
  font-weight: 600;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: var(--olive);
}

/* Heading */
.about__heading {
  font-family: 'Playfair Display', serif;
  font-size: 2.6rem;
  font-weight: 400;
  line-height: 1.25;
  margin: 0;
  color: var(--text-dark);
}

.about__heading em {
  font-style: italic;
}

/* Paragraphs */
.about__paragraphs {
  display: flex;
  flex-direction: column;
  gap: 14px;
}

.about__paragraph {
  font-size: 0.95rem;
  line-height: 1.8;
  color: var(--text-mid);
  font-weight: 300;
  margin: 0;
}

/* Features grid */
.about__features {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px 32px;
  margin-top: 8px;
  padding: 24px;
  background: var(--cream);
  border-radius: 10px;
}

.about__feature {
  display: flex;
  gap: 12px;
  align-items: flex-start;
}

.feature__icon {
  font-size: 1.1rem;
  margin-top: 2px;
  flex-shrink: 0;
}

.feature__content {
  display: flex;
  flex-direction: column;
  gap: 4px;
}

.feature__title {
  font-size: 0.85rem;
  font-weight: 600;
  color: var(--text-dark);
  margin: 0;
  letter-spacing: 0.02em;
}

.feature__description {
  font-size: 0.8rem;
  line-height: 1.6;
  color: var(--text-mid);
  font-weight: 300;
  margin: 0;
}
</style>
