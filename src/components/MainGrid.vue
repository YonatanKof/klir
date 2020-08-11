<template>
  <section class="main-grid-warp">
    <div class="main-grid">
      <SideBar />
      <MainBanner />
      <SmallBannerGrid />
    </div>
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
@import "../styles/variables";

.main-grid-warp {
  padding: var(--main-padding);
  @media screen and (max-width: $width-sm) {
    padding-top: 0;
  }
}
.main-grid {
  display: grid;
  max-width: var(--max-width);
  margin: 0 auto;
  grid-template-areas:
    "sidebar main-banner"
    "sidebar small-banner-grid";
  grid-gap: 32px;
  @media screen and (max-width: $width-md) {
    grid-gap: 24px;
    grid-template-areas:
      "main-banner main-banner"
      "sidebar small-banner-grid";
    grid-template-columns: auto 1fr;
  }
  @media screen and (max-width: $width-sm) {
    grid-template-areas:
      "main-banner"
      "sidebar"
      "small-banner-grid";
    grid-template-columns: 1fr;
    grid-template-rows: 320px auto auto;
  }
}
</style>