<template>
  <div class="small-banner-grid">
    <SmallBanner />
    <SmallBanner />
    <SmallBanner />
    <SmallBanner />
    <SmallBanner />
    <SmallBanner />
    <SmallBanner />
    <SmallBanner />
    <SmallBanner />
    <SmallBanner />
  </div>
</template>

<script>
import SmallBanner from "./SmallBanner.vue";

export default {
  name: "SmallBannerGrid",
  components: {
    SmallBanner,
  },
};
</script>

<style lang="scss">
@import '../styles/variables';

.small-banner-grid {
  display: grid;
  place-items: start;
  grid-gap: 24px;
  grid-template-columns: repeat(5, 1fr);
  grid-area: small-banner-grid;
  @media screen and (max-width: $width-lg) {
    grid-template-columns: repeat(4, 1fr);
    grid-gap: 16px;
  }
  @media screen and (max-width: $width-md) {
    grid-template-columns: repeat(3, 1fr);
  }
  @media screen and (max-width: $width-sm) {
    grid-template-columns: repeat(2, 1fr);
  }
}

.small-banner-grid > * {
  width: 100%;
}
.small-banner-grid > [style^="--aspect-ratio"]::before {
  content: "";
  display: inline-block;
  width: 1px;
  height: 0;
  padding-bottom: calc(100% / (var(--aspect-ratio)));
}
</style>