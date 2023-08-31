<script setup>
defineProps({
  aboutIconImage: String,
  aboutIconHeadline: String
})
</script>
<template>
  <div class="icon-wrapper">
    <div class="img-container">
      <img :src="aboutIconImage" alt="" />
    </div>

    <h1>{{ aboutIconHeadline }}</h1>
  </div>
</template>

<style lang="scss" scoped>
.icon-wrapper {
  display: flex;
  align-items: center;
  .img-container {
    height: 60px;
    width: 60px;
    padding-right: 20px;

    img {
      width: 100%;
      height: 100%;
    }
  }

  h1 {
    font-family: 'Saira Condensed', sans-serif;
    font-weight: bold;
    text-transform: uppercase;
    letter-spacing: 0.1rem;
    white-space: nowrap;
    color: white;
  }
}
</style>
