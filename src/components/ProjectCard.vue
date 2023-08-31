<script setup>
defineProps({
  project: {
    type: Object,
    required: true
  }
})
</script>

<template>
  <div class="project-card">
    <img :src="project.imageUrl" alt="" />
    <h2>{{ project.projectName }}</h2>
  </div>
</template>

<style lang="scss" scoped>
.project-card {
  position: relative;
  cursor: zoom-in;

  img {
    height: 100%;
    width: 100%;
    background-size: cover;
    object-fit: cover;
    filter: brightness(50%);
    transition: 500ms ease-in-out;
    &:hover {
      filter: brightness(100%);
    }
  }

  h2 {
    font-family: 'Saira Condensed', sans-serif;
    font-weight: 400;
    font-size: 1.5rem;
    text-transform: uppercase;
    color: white;
    margin-left: 15px;
    position: absolute;
    top: 0;
  }
}
</style>
