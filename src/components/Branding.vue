<script setup>
import { Icon } from '@iconify/vue'
</script>

<template>
  <div class="branding-social-wrapper">
    <div class="social-media-container">
      <a href="https://www.linkedin.com/company/doseengineering"
        ><Icon icon="pajamas:linkedin" color="white" width="28" height="28"
      /></a>
      <a href=""><Icon icon="fe:facebook" color="white" width="28" height="28" /></a>
      <a href=""><Icon icon="teenyicons:instagram-solid" color="white" width="28" height="28" /></a>
    </div>
    <h1>dose engineering</h1>
  </div>
</template>

<style lang="scss" scoped>
.branding-social-wrapper {
  display: flex;
  flex-direction: column-reverse;
  align-items: center;
  justify-content: space-between;
  height: 600px;
  width: 70px;
  background-color: #00000041;

  h1 {
    font-family: 'Saira Condensed', sans-serif;
    font-size: 2rem;
    font-weight: 400;
    letter-spacing: 0.35rem;
    color: white;
    white-space: nowrap;
    text-transform: uppercase;
    transform: rotate(-90deg);
    margin-top: 150px;
  }

  .social-media-container {
    display: flex;
    height: 200px;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 25px;

    a {
      opacity: 0.5;
      transition: 0.2s ease-in-out;

      &:hover {
        opacity: 1;
      }
    }
  }
}
</style>
