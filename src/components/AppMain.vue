<script>
import AppBluestripe from "@/components/AppBluestripe.vue";
import AppCard from "@/components/AppCard.vue";

export default {
    name: "AppMain",
    components: { AppBluestripe, AppCard },
    props: {
        dcComics: Array,
    }
}
</script>

<template>
    <main>
        <div class="container">
            <p>CURRENT SERIES</p>
            <div class="row">
                <AppCard :dcComics="dcComics" />
            </div>
            <button>LOAD MORE</button>
        </div>
        <AppBluestripe />
    </main>
</template>

<style lang="scss" scoped>
@use "@/scss/variables" as *;

main {
    color: white;

    .container {
        flex-direction: column;
        position: relative;

        p {
            position: absolute;
            left: -5%;
            bottom: 100%;
            background-color: $blue;
            padding: 0.5rem 1rem;
            transform: translateY(50%);
        }
    }

    .row {
        display: flex;
        flex-wrap: wrap;
        padding: 2rem 0rem 1rem;
        margin: 0 -10px;
    }

    button {
        color: white;
        background-color: $blue;
        padding: 0.5rem 3rem;
        margin-bottom: 1rem;
    }
}
</style>
