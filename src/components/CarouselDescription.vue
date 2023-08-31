<template>
    <div class="carousel-description-wrap">
        <span class="service-headline">
            <h1>{{ service.serviceHeadline }}</h1>
        </span>
        <span class="service-description">
            <p>{{ service.serviceDescription }}</p>
        </span>
    </div>
</template>

<script setup>
defineProps ({
    service: {
        Type: Object,
        required: true,
    },
})
</script>

<style lang="scss" scoped>

.carousel-description-wrap {
    display: flex;
    flex-direction: column;
    align-items: end;

    h1 {
        font-family: 'Saira Condensed', sans-serif;
        font-size: 2.5rem;
        font-weight: bold;
        text-transform: uppercase;
        text-align: end;
        letter-spacing: 0.1rem;
        color: white;
        margin: 0;
    }

    .service-description {
        width: 65%;

        p {
            font-family: 'Inter', sans-serif;
            color: #dadada;
            text-align: end;
            line-height: 1.5rem;
        }
    }
}

</style>