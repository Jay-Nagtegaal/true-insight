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
  display: flex;
  align-items: center;
  gap: 64px;
  max-width: 1100px;
  margin: 0 auto;
  padding: 80px 32px;
}

/* ── Left: Image column ── */
.about__image-wrapper {
  flex: 1;
  position: relative;
  max-width: 420px;
}

.about__image {
  width: 100%;
  height: 500px;
  object-fit: cover;
  border-radius: 16px;
  display: block;
}

/* Stat overlay */
.about__stat {
  position: absolute;
  top: 50%;
  right: -24px;
  transform: translateY(-50%);
  background: #ffffff;
  border-radius: 10px;
  padding: 16px 22px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
  display: flex;
  flex-direction: column;
  align-items: center;
}

.about__stat-number {
  font-size: 2rem;
  font-weight: 700;
  color: #111;
  line-height: 1;
}

.about__stat-label {
  font-size: 0.78rem;
  color: #777;
  margin-top: 4px;
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
  font-size: 0.75rem;
  font-weight: 600;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: #777;
}

/* Heading */
.about__heading {
  font-size: 2.4rem;
  font-weight: 700;
  line-height: 1.25;
  margin: 0;
  color: #111;
}

.about__heading em {
  font-style: italic;
  font-weight: 700;
}

/* Paragraphs */
.about__paragraphs {
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.about__paragraph {
  font-size: 0.97rem;
  line-height: 1.7;
  color: #444;
  margin: 0;
}

/* Features grid */
.about__features {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px 32px;
  margin-top: 8px;
}

.about__feature {
  display: flex;
  gap: 12px;
  align-items: flex-start;
}

.feature__icon {
  font-size: 1.2rem;
  margin-top: 2px;
  flex-shrink: 0;
}

.feature__content {
  display: flex;
  flex-direction: column;
  gap: 4px;
}

.feature__title {
  font-size: 0.9rem;
  font-weight: 700;
  color: #111;
  margin: 0;
}

.feature__description {
  font-size: 0.82rem;
  line-height: 1.55;
  color: #555;
  margin: 0;
}
</style>
