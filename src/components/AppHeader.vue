<template>
  <header>
    <div class="header-warp">
      <div class="header-start">
        <img alt="סמליל קליר" src="../assets/logo.png" />
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  // display: flex;
  background-color: var(--main-color);
  padding: 0 var(--main-padding);
  .header-warp {
    height: var(--header-height);
    align-items: center;
    margin: 0 auto;
    max-width: var(--max-width);
    display: flex;
    justify-content: space-between;
    flex-direction: row;
    align-items: center;
  }
  img {
    height: 48px;
  }
}
</style>