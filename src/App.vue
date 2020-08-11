<template>
  <div id="app">
    <AppHeader />
    <HelloWorld msg="ברוכים הבאים לקליר!"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import AppHeader from './components/AppHeader.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    AppHeader
  }
}
</script>

<style lang="scss">
@import "./styles/reset";
@import "./styles/variables";

#app {
  direction: rtl;
  font-family: var(--font-family--body);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  // text-align: center;
  // color: #2c3e50;
  // margin-top: 60px;
}
</style>
