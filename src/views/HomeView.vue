<script setup>
import { ref, onMounted } from 'vue'
import ServicesCarousel from '../components/ServicesCarousel.vue'
import CarouselSlide from '../components/CarouselSlide.vue'
import CarouselDescription from '../components/CarouselDescription.vue'
import AboutSection from '../components/AboutSection.vue'
import ProjectsSection from '../components/ProjectsSection.vue'
import IntegrationSection from '../components/IntegrationSection.vue'
import LocationSection from '../components/LocationSection.vue'
import NextButton from '../components/Buttons/NextButton.vue'
import PreviewButton from '../components/Buttons/PreviewButton.vue'
import Branding from '../components/Branding.vue'
import GotoServicesButton from '../components/Buttons/GotoServicesButton.vue'

const services = [
  {
    serviceImage: './src/assets/images/services/image_01.jpg',
    serviceHeadline: 'convert all your assets to the digital world',
    serviceDescription:'Transforming laser scanning data into intelligent BIM models is our expertise. We optimize your design phase and minimize risks in existing projects, giving you a competitive advantage.'
  },
  {
    serviceImage: './src/assets/images/services/image_02.jpg',
    serviceHeadline: 'revolutionizing bim with tailor-made software',
    serviceDescription:"Through Dynamo scripts and Revit Add-ins, we offer customized solutions that optimize workflows, automate tasks, and enhance Revit's functionality, ensuring outstanding results for your construction projects."
  },
  {
    serviceImage: './src/assets/images/services/image_03.jpg',
    serviceHeadline: 'Turning your products into BIM realities',
    serviceDescription:'We specialize in developing top-quality Revit families, combining visual excellence with exceptional functionality. Our optimized families streamline operations, allowing you to focus on your project with confidence.'
  },
  {
    serviceImage: './src/assets/images/services/image_04.jpg',
    serviceHeadline: 'Transforming your projects into precise 3D masterpieces.',
    serviceDescription:'Transforming laser scanning data into intelligent BIM models is our expertise. We optimize your design phase and minimize risks in existing projects, giving you a competitive advantage.'
  }
]

const currentSlide = ref(1)
const getSlideCount = ref(null)

// next //
const nextSlide = () => {
  if (currentSlide.value === getSlideCount.value) {
    currentSlide.value = 1
    return;
  }
  currentSlide.value ++
}

// prew //

const prevSlide = () => {
  if (currentSlide.value === 1) {
    currentSlide.value = getSlideCount.value
    return;
  }
  currentSlide.value --
}

onMounted(() => {
  getSlideCount.value = document.querySelectorAll('.slide').length
});
</script>

<template>
  <main>
    <section id="services">
      <ServicesCarousel class="service-carousel">
          <CarouselSlide v-show="currentSlide === index + 1" v-for="(service, index) in services" :service="service" :key="index"/>
        <div class="service-description-section">
          <div class="counter-buttons">
            <div class="sliding-buttons">
              <PreviewButton @click="prevSlide"/>
              <NextButton @click="nextSlide"/>
            </div>

            <div class="counter">
              <span class="current-slide"><h1>0{{ currentSlide }}</h1></span>
              <span class="total-slides"><h3>/0{{ getSlideCount }}</h3></span>
            </div>
          </div>

          <div class="service-description-wrap">
            <CarouselDescription v-show="currentSlide === index + 1" v-for="(service, index) in services" :service="service" :key="index"/>
            <GotoServicesButton style="margin-top: 40px;"/>
          </div>
        </div>

        <Branding class="branding"/>
      </ServicesCarousel>
    </section>
    <section id="about">
      <AboutSection />
    </section>

    <section id="projects">
      <ProjectsSection />
    </section>

    <section class="integration">
      <IntegrationSection />
    </section>

    <section class="location">
      <LocationSection />
    </section>
  </main>
</template>

<style lang="scss" scoped>
.service-carousel {
  position: relative;

  .service-description-section {
    display: flex;
    align-items: start;
    justify-content: space-between;
    width: 80%;
    max-width: 1440px;
    height: 60%;
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);

    .service-description-wrap {
      display: flex;
      width: calc(100% - 300px);
      flex-direction: column;
      align-items: end;
      justify-content: space-evenly;
    }

    .counter-buttons {
      display: flex;
      height: 100%;
      width: 300px;
      flex-direction: column;
      justify-content: space-between;

      .sliding-buttons {
        display: flex;
        justify-content: space-between;
      }

      .counter {
        display: flex;
        align-items: start;
        height: 30%;

        h1 {
          font-family: 'Saira Condensed', sans-serif;
          text-align: end;
          width: 90px;
          font-weight: 400;
          font-size: 6rem;
          letter-spacing: 0.2rem;
          color: white;
          margin: 0;
          padding: 0;
          opacity: 0.8;
        }

        h3 {
          font-family: 'Saira Condensed', sans-serif;
          font-weight: 400;
          font-size: 2rem;
          letter-spacing: 0.2rem;
          color: white;
          opacity: 0.5;
          margin-left: 5px;
        }
      }
    }
  }

  .branding {
    position: absolute;
    top: 0;
    left: 0;
  }
}
</style>
