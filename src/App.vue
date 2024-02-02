<script setup>
import AppHeader from "./components/AppHeader.vue"
import AppMain from "./components/AppMain.vue"
import AppFooter from "./components/AppFooter.vue"
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppFooter />
</template>

<style>
body {
  background-color: black;
}

a {
  text-decoration: none;
}

li {
  list-style-type: none;
}

ul {
  padding: 0;
}
</style>
