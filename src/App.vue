<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  name: "DC-Comics",
  components: {
    AppHeader,
    AppMain,
    AppFooter
  }
}

</script>

<template>
  <AppHeader />
  <AppMain />
  <AppFooter />
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background-color: #1C1C1C;
  font-family: 'Open Sans', sans-serif;
}

a {
  text-decoration: none;
}

li {
  list-style-type: none;
}

.container {
  width: 70%;
  margin: 0 auto;
  height: 100%;
}
</style>
