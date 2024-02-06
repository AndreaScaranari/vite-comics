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
            <div class="row">
                <AppCard :dcComics="dcComics" />
            </div>
        </div>
        <AppBluestripe />
    </main>
</template>

<style lang="scss" scoped>
main {
    color: white;

    .row {
        display: flex;
        flex-wrap: wrap;
        padding: 2rem 0rem;
        margin: 0 -10px;
    }
}
</style>
