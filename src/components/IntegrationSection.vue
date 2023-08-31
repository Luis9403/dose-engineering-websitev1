<script setup>
import SphereElement from './SphereElement.vue'
</script>

<template>
  <div class="integration-section-wrapper">
    <div class="integration-section-headline">
      <h1>why <strong>choose us</strong></h1>
    </div>
    <SphereElement class="sphere-element" />
  </div>
</template>

<style lang="scss" scoped>
.integration-section-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 700px;
  padding-top: 40px;
  position: relative;

  .integration-section-headline {
    h1 {
      font-family: 'Saira Condensed';
      font-weight: 300;
      font-size: 1.8em;
      color: white;
      text-transform: uppercase;
      letter-spacing: 0.2em;
    }
  }

  .sphere-element {
    position: absolute;
    top: 50%;
    left: 50%;
  }
}
</style>
