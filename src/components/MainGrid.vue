<template>
  <section class="main-grid">
    <SideBar />
    <MainBanner />
    <SmallBannerGrid />
  </section>
</template>

<script>
import SideBar from "./SideBar.vue";
import MainBanner from "./MainBanner.vue";
import SmallBannerGrid from "./SmallBannerGrid.vue";

export default {
  name: "MainGrid",
  components: {
    SideBar,
    MainBanner,
    SmallBannerGrid,
  },
};
</script>

<style lang="scss">
.main-grid {
  display: grid;
  background-color: powderblue;
  padding: var(--main-padding);
  max-width: var(--max-width);
  margin: 0 auto;
  grid-template-areas:
    "sidebar main-banner"
    "sidebar small-banner-grid";
  grid-gap: 32px;
}
</style>