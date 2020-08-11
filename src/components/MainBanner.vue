<template>
  <div class="main-banner">
    <img src="../assets/main-banner-2.jpg" alt="main banner" />
  </div>
</template>

<style lang="scss">
@import '../styles/variables';

.main-banner {
  overflow: hidden;
  border-radius: 8px;
  background-color: purple;
  grid-area: main-banner;
  padding: 0;
  img {
    display: block;
    max-width: 100%;
    height: 100%;
    object-fit: cover;
  }
  @media screen and (max-width: $width-sm) {
    margin: 0 calc(var(--main-padding) * -2);
  }
}
</style>