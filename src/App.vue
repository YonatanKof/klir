<template>
  <div id="app">
    <AppHeader />
    <MainGrid />
  </div>
</template>

<script>
import MainGrid from "./components/MainGrid.vue";
import AppHeader from "./components/AppHeader.vue";

export default {
  name: "App",
  components: {
    MainGrid,
    AppHeader,
  },
};
</script>

<style lang="scss">
@import "./styles/reset";
@import "./styles/variables";

#app {
  overflow-x: hidden;
  direction: rtl;
  font-family: var(--font-family--body);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
