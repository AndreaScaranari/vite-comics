<script>
export default {
    name: "AppJumbotron",
    data: () => ({
        jumbotron: "jumbotron.jpg"
    }),
    methods: {
        createImagePath(imgName) {
            const url = new URL(`../assets/img/${imgName}`, import.meta.url);
            return url.href
        }
    }
}
</script>

<template>
    <div class="jumbotron"></div>
</template>

<style lang="scss" scoped>
.jumbotron {
    height: 500px;
    width: 100%;
    background-image: url("@/assets/img/jumbotron.jpg");
    background-size: cover;
}
</style>