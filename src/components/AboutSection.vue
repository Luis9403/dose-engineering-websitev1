<script setup>
import AboutIcon from './Icons/AboutIcon.vue'
</script>

<template>
  <div class="about-section-container">
    <div class="about-section-headline">
      <h1>about <strong>dose engineering</strong></h1>
    </div>
    <div class="about-section-description-wrapper">
      <div class="column">
        <div class="first-description-wrapper column-inside">
          <h2>we <strong>stand besides</strong> our <strong>clients</strong>.</h2>
          <p>
            At DOSE Engineering, we take pride in driving change within the construction industry.
            Our mission is to enhance efficiency across all processes, from design to construction,
            through BIM methodology. We optimize project lifecycle stages, enabling smoother
            collaboration and informed decision-making.
          </p>
        </div>
      </div>

      <div class="column">
        <div class="second-description-wrapper column-inside">
          <h2><strong>innovation</strong> is key to <strong>progress</strong></h2>
          <p>
            At DOSE Engineering, we take pride in driving change within the construction industry.
            Our mission is to enhance efficiency across all processes, from design to construction,
            through BIM methodology. We optimize project lifecycle stages, enabling smoother
            collaboration and informed decision-making.
          </p>
        </div>
      </div>

      <div class="column">
        <div class="third-description-wrapper column-inside">
          <AboutIcon
            about-icon-image="./src/assets/icons/icons8-gears-100.png"
            about-icon-headline="connecting workflows"
          />
          <AboutIcon
            about-icon-image="./src/assets/icons/icons8-safety-hat-64.png"
            about-icon-headline="building everything"
          />
          <AboutIcon
            about-icon-image="./src/assets/icons/octahedron.svg"
            about-icon-headline="digitalizing the world"
          />
          <AboutIcon
            about-icon-image="./src/assets/icons/accelerate-arrows.svg"
            about-icon-headline="getting ahead"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.about-section-container {
  display: flex;
  height: 700px;
  flex-direction: column;
  align-items: center;
  .about-section-headline {
    h1 {
      font-family: 'Saira Condensed';
      font-weight: 300;
      font-size: 1.8em;
      color: white;
      text-transform: uppercase;
      letter-spacing: 0.2em;
    }
  }

  .about-section-description-wrapper {
    display: grid;
    width: 70%;
    height: 600px;
    grid-template-columns: 1fr 1fr 1fr;

    .column {
      display: flex;
      justify-content: center;
      border-left: 1px solid #ffffff11;
      border-right: 1px solid #ffffff11;

      .column-inside {
        width: 80%;

        h2 {
          font-family: 'Inter', sans-serif;
          font-weight: bold;
          font-size: 1.8em;
          color: #646464;
          line-height: 2rem;

          strong {
            color: white;
          }
        }

        p {
          font-family: 'Inter', sans-serif;
          font-size: 1.2em;
          color: white;
          line-height: 2.5rem;
          padding-top: 10px;
        }
      }
    }

    .third-description-wrapper {
      display: flex;
      flex-direction: column;
      justify-content: space-around;
      align-items: left;
    }
  }
}
</style>
