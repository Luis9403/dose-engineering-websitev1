<script setup>
import { Icon } from '@iconify/vue'
import ProjectCard from './ProjectCard.vue'

const projectList = [
  {
    imageUrl: './src/assets/images/projects/img_1.jpg',
    projectName: 'Fire Pump Room',
    projectDescription: 'Lorem ipsum'
  },
  {
    imageUrl: './src/assets/images/projects/img_2.jpg',
    projectName: 'Fire Pump Room',
    projectDescription: 'Lorem ipsum'
  },
  {
    imageUrl: './src/assets/images/projects/img_3.jpg',
    projectName: 'Fire Pump Room',
    projectDescription: 'Lorem ipsum'
  },
  {
    imageUrl: './src/assets/images/projects/img_4.jpg',
    projectName: 'Fire Pump Room',
    projectDescription: 'Lorem ipsum'
  },
  {
    imageUrl: './src/assets/images/projects/img_5.jpg',
    projectName: 'Fire Pump Room',
    projectDescription: 'Lorem ipsum'
  },
  {
    imageUrl: './src/assets/images/projects/img_6.jpg',
    projectName: 'Fire Pump Room',
    projectDescription: 'Lorem ipsum'
  },
  {
    imageUrl: './src/assets/images/projects/img_7.jpg',
    projectName: 'Fire Pump Room',
    projectDescription: 'Lorem ipsum'
  },
  {
    imageUrl: './src/assets/images/projects/img_8.jpg',
    projectName: 'Fire Pump Room',
    projectDescription: 'Lorem ipsum'
  }
]
</script>

<template>
  <div class="projects-section-container">
    <div class="project-section-headline">
      <h1>our <strong>projects</strong></h1>
    </div>
    <div class="project-list-wrapper">
      <ProjectCard class="project-card" v-for="project in projectList" :project="project" />
    </div>
    <div class="navigation-buttons-wrapper">
      <button class="next-button button">
        <Icon icon="solar:arrow-up-outline" width="22px" height="22px" :rotate="-1" color="white" />
        <p>Prew</p>
      </button>
      <button class="preview-button button">
        <p>Next</p>
        <Icon icon="solar:arrow-up-outline" width="22px" height="22px" :rotate="1" color="white" />
      </button>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.projects-section-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 800px;
  margin-top: 40px;
  position: relative;

  .project-section-headline {
    h1 {
      font-family: 'Saira Condensed';
      font-weight: 300;
      font-size: 1.8em;
      color: white;
      text-transform: uppercase;
      letter-spacing: 0.2em;
    }
  }

  .project-list-wrapper {
    display: flex;
    width: 100%;
    overflow: hidden;
    height: 100%;

    .project-card {
      display: flex;
      flex: 0 0 25%;
      overflow-x: auto;
    }
  }

  .navigation-buttons-wrapper {
    display: flex;
    width: 95%;
    align-items: center;
    justify-content: space-between;
    position: absolute;
    top: 50%;

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
        cursor: pointer;
        opacity: 1;
      }

      p {
        font-family: 'Saira Condensed', sans-serif;
        font-size: 1.3rem;
        color: white;
      }
    }
  }
}
</style>
