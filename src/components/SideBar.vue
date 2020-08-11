<template>
  <aside class="side-bar">
    <hr />
    <button>צרו הזמנה חדשה</button>
    <hr />
    <div class="cards">
      <InfoCard card-title="קו אשראי" card-value="₪20,000" card-icon-name="Balance">
        <IconDark />
      </InfoCard>
      <InfoCard card-title="יתרת חשבון" card-value="₪2,048" card-icon-name="Show me the money">
        <IconBright />
      </InfoCard>
    </div>
  </aside>
</template>

<script>
import InfoCard from "./InfoCard.vue";
import IconDark from "./icons/IconDark.vue";
import IconBright from "./icons/IconBright.vue";

export default {
  name: "SideBar",
  components: {
    InfoCard,
    IconDark,
    IconBright
  },
};
</script>

<style lang="scss">
@import "../styles/variables";

.side-bar {
  width: 208px;
  height: max-content;
  grid-area: sidebar;
}
button {
  padding: 16px;
  width: 100%;
  font-size: 1em;
}
hr,
button {
  margin: 0;
  margin-bottom: 16px;
}
@media screen and (max-width: $width-sm) {
  .side-bar {
    width: 100%;
  }
  .cards {
    display: flex;
    align-items: center;
    margin: 0 auto;
    justify-content: space-between;
    flex-direction: row;
    align-items: center;
  }
}
</style>