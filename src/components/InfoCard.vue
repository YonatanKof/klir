<template>
  <div class="card">
    <div class="card-info">
      <h3>{{ cardTitle }}</h3>
      <h2>{{ cardValue }}</h2>
    </div>
    <IconBase
      class
      :icon-name="cardIconName"
      icon-color="var(--main-strong)"
      width="48"
      height="48"
    >
      <slot />
    </IconBase>
  </div>
</template>

<script>
import IconBase from "./IconBase.vue";
// import IconKof from "./icons/IconKof.vue";

export default {
  name: "InfoCard",
  props: ["cardTitle", "cardValue", "cardIconName"],
  components: {
    IconBase
  },
};
</script>

<style lang="scss">
@import "../styles/variables";

.card {
  padding: 16px;
  width: 100%;
  background-color: powderblue;
  margin-bottom: 16px;
  display: flex;
  justify-content: space-between;
  flex-direction: row;
  align-items: center;
  .card-info {
    *:first-child {
      margin-bottom: 8px;
    }
  }
  @media screen and (max-width: $width-sm) {
    margin-bottom: 0;
    &:first-child {
      margin-inline-end: 16px;
    }
  }
}
</style>