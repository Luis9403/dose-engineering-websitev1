<script setup>
import { Icon } from '@iconify/vue'
</script>

<template>
  <button class="next-button button">
    <p>Next</p>
    <Icon icon="solar:arrow-up-outline" width="22px" height="22px" :rotate="1" color="white" />
  </button>
</template>

<style lang="scss" scoped>
.button {
  display: flex;
  width: 80px;
  justify-content: space-between;
  align-items: center;
  background-color: transparent;
  border: 0;
  opacity: 0.6;
  transition: 200ms ease-in-out;

  &:hover {
    opacity: 1;
    cursor: pointer;
  }
}

p {
  font-family: 'Saira Condensed', sans-serif;
  font-weight: 300;
  font-size: 1.3rem;
  color: white;
}
</style>
