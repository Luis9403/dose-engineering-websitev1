<script setup></script>

<template>
  <div class="spheres-wrapper">
    <span class="outer-sphere sphere"></span>
    <span class="inner-sphere sphere"></span>
  </div>
</template>

<style lang="scss" scoped>
.spheres-wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;

  .outer-sphere {
    width: 400px;
    height: 400px;
    position: absolute;
  }

  .inner-sphere {
    width: 300px;
    height: 300px;
    position: absolute;
  }

  .sphere {
    border: 1px solid black;
    border-radius: 50%;
  }
}
</style>
