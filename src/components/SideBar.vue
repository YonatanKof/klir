<template>
  <aside class="side-bar">
    <hr />
    <button>צרו הזמנה חדשה</button>
    <hr />
    <div class="cards">
      <div class="card">
        <h3>קו אשראי</h3>
        <h2>₪20,000</h2>
      </div>
      <div class="card">
        <h3>יתרת חשבון</h3>
        <h2>₪2,048</h2>
      </div>
    </div>
  </aside>
</template>

<style lang="scss">
@import "../styles/variables";

.side-bar {
  width: 208px;
  height: max-content;
  grid-area: sidebar;
}
.card,
button {
  padding: 16px;
  width: 100%;
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