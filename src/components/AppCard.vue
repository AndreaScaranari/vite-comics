<script>
export default {
    name: "AppCard",
    data: () => ({}),
    props: {
        dcComics: Array,
    },
    methods: {
        createImagePath(imgName) {
            const url = new URL(`../assets/img/${imgName}`, import.meta.url);
            return url.href
        }
    }
}
</script>

<template>
    <div v-for="comic in dcComics" class="col">
        <div class="card-img">
            <img :src="comic.thumb" alt="">
        </div>
        <div class="card-text">
            <h3>{{ comic.series }}</h3>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.col {
    width: calc(100% / 6);
    padding: 10px;

    .card-img {
        width: 100%;

        img {
            width: 100%;
            aspect-ratio: 1 / 1;
            object-fit: cover;
            object-position: 0% 0%;
        }

    }

    h3 {
        padding-top: 1rem;
        font-size: 0.8rem;
        text-transform: uppercase;
    }
}
</style>