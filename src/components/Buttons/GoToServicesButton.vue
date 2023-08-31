<script setup>
import { Icon } from '@iconify/vue'
</script>

<template>
  <button class="services-link">
    <div class="go-to-services-container">
      <p>Go to services</p>
      <Icon icon="solar:arrow-up-outline" width="18px" height="18px" :rotate="1" />
    </div>
  </button>
</template>

<style lang="scss" scoped>
.services-link {
  display: flex;
  align-items: center;
  justify-content: center;
  border: 0;
  border-radius: 50px;
  width: 200px;
  height: 50px;

  &:hover {
    cursor: pointer;
  }

  .go-to-services-container {
    display: flex;
    width: 100%;
    justify-content: space-evenly;
    align-items: center;

    p {
      font-family: 'Saira Condensed', sans-serif;
      font-weight: bold;
      font-size: 1.5em;
      text-transform: uppercase;
    }
  }
}
</style>
