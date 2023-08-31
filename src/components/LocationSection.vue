<template>
  <div class="location-section-wrapper">
    <div class="location-section-headline">
      <h1>our <strong>experience</strong></h1>
    </div>

    <div class="world-wrapper">
      <img src="../assets/world-img.svg" alt="" />
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
.location-section-wrapper {
  display: flex;
  height: 800px;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  .location-section-headline {
    h1 {
      font-family: 'Saira Condensed';
      font-weight: 300;
      font-size: 1.8em;
      color: white;
      text-transform: uppercase;
      letter-spacing: 0.2em;
    }
  }

  .world-wrapper {
    display: flex;
    justify-content: center;
    width: 90%;
    height: 700px;
    img {
      height: 100%;
      background-size: cover;
      transform: scaleX(1.1);
    }
  }
}
</style>
