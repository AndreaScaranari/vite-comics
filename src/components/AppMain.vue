<script>
import AppBluestripe from "@/components/AppBluestripe.vue";

export default {
    name: "AppMain",
    components: { AppBluestripe }
}
</script>

<template>
    <main>
        <div class="container">
            <h1>Content goes here</h1>
        </div>
        <AppBluestripe />
    </main>
</template>

<style lang="scss" scoped>
main {
    color: white;

    .container {
        height: 120px;
    }
}
</style>
