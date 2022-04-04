<template>
  <div id="app">
    <!-- Header con logo e nav -->
    <classic-shop-header />
    <!-- Main con le varie sotto-sezioni -->
    <classic-shop-main />
    <!-- Footer con link e pagamenti -->
    <classic-shop-footer />
  </div>
</template>

<script>
import classicShopHeader from "./components/classicShopHeader.vue";
import classicShopMain from "./components/classicShopMain.vue";
import classicShopFooter from "./components/classicShopFooter.vue";

export default {
  name: "App",
  components: {
    classicShopHeader,
    classicShopMain,
    classicShopFooter,
  },
};
</script>

<style lang="scss">
@import "./assets/styles/style.scss";
#app {
  font-family: "PT Sans", Helvetica, Arial, sans-serif;
  // color: $confetti;
}
</style>
