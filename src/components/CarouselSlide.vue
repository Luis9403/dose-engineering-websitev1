<template>
<transition name="slide">
    <div class="slide">

        <img :src="service.serviceImage" alt="">

    </div>
</transition>
    
</template>

<script setup>
defineProps({
    service: {
        type: Object,
        required: true,
    }
})
</script>

<style lang="scss" scoped>
.slide {
    width: 100%;
    height: 100%;

    img {
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
        object-fit: cover;
        filter: brightness(0.5);
    }
}

.slide-enter-active,
.slide-leave-active {
    transition: opacity 0.5s ease-in-out;
  }

.slide-enter-from,
.slide-leave-to {
    opacity: 0;
}

.slide-enter-to,
.slide-leave-from {
    opacity: 1;
}

</style>