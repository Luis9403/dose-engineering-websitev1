<script setup>
import { RouterLink } from 'vue-router'

window.onscroll = function () {
  scrollNavbar()
}

function scrollNavbar() {
  if (document.body.scrollTop > 100 || document.documentElement.scrollTop > 100) {
    const navBarContainer = document.getElementById('navbar')
    navBarContainer.style.backdropFilter = 'blur(4px)'
    navBarContainer.style.borderBottom = '1px solid'
    navBarContainer.style.borderImage =
      'linear-gradient(to right, #ffffff0a, #ffffffbb, #ffffff0a) 20'
  } else {
    const navBarContainer = document.getElementById('navbar')
    navBarContainer.style.backdropFilter = 'blur(0px)'
    navBarContainer.style.borderBottom = '1px solid transparent'
    navBarContainer.style.borderImage = '0'
  }
}
</script>

<template>
  <header id="navbar">
    <nav class="nav-bar">
      <RouterLink class="link-button" to="/">home</RouterLink>
      <RouterLink class="link-button" to="/services">services</RouterLink>

      <RouterLink class="dose-logo" to="/">
        <img src="../assets/dose-logo.svg" alt="" />
      </RouterLink>

      <RouterLink class="link-button" to="#about">about</RouterLink>
      <RouterLink class="link-button" to="#contact">contact</RouterLink>
    </nav>
  </header>
</template>

<style lang="scss" scoped>
#navbar {
  width: 100%;
  position: fixed;
  top: 0;
  transition: 0.4s ease-in-out;
  z-index: 99;

  .nav-bar {
    display: flex;
    justify-content: space-evenly;
    align-items: center;

    .link-button {
      font-family: 'Saira Condensed', sans-serif;
      font-size: 20px;
      font-weight: 400;
      color: white;
      text-decoration: none;
      text-transform: uppercase;
      letter-spacing: 0.2rem;
      border-bottom: 1px solid transparent;
      opacity: 0.6;
      transition: 250ms ease-in-out;

      &:hover {
        border-bottom: 1px solid white;
        opacity: 1;
      }
    }

    img {
      width: 90px;
      height: 90px;
    }
  }
}
</style>
