<template>
  <div id="app">
    <HeaderComp />
    <MainComp />
    <FooterComp />
  </div>
</template>

<script>
import "bootstrap";
import HeaderComp from "./components/HeaderComp.vue";
import MainComp from "./components/MainComp.vue";
import FooterComp from "./components/FooterComp.vue";

export default {
  name: "App",
  components: {
    HeaderComp,
    MainComp,
    FooterComp,
  },
};
</script>

<style lang="scss">
// importiamo bootstrap
@import "bootstrap/dist/css/bootstrap.min.css";
// importiamo gli style
@import "./assets/scss/style.scss";
// importiamo il tipo di font
@import url("https://fonts.googleapis.com/css2?family=Hurricane&family=Nunito:ital,wght@0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");

#app {
  font-family: "Nunito", sans-serif;
}
</style>
