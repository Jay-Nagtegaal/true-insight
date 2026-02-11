<script setup>

</script>

<template>
  <div class="nav-bar">
    <div class="nav-bar-left">
      <div class="personal-information">
        <div class="phone-number"> +31 6 1234 5678</div>
        <div class="email">marion.gulpers@trueinsight.nl</div>
      </div>
      <div class="title">
        <h1>True Insight</h1>
        Integrale Geneeskunde
      </div>
    </div>
    <div class="nav-bar-right">
      <div class="region-information">
        <p>Regio Amsterdam - Amstelveen - Aalsmeer</p>
      </div>
      <div class="nav-bar-buttons">
        <button class="button">Home</button>
        <button class="button">Over Mij</button>
        <button class="button">Methodieken</button>
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
  display: flex;
  width: 90%;
  height: 100px;
  background: white;
  border-bottom: black solid 1px;
  border-top: black solid 1px;
  margin-left: 50px;
  margin-right: 50px;
  padding-left: 50px;
  padding-right: 50px;
  flex-direction: row;
  justify-content: space-between;
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