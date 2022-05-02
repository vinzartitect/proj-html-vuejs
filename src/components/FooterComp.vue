<template>
  <footer>
    <FooterNav />
    <FooterBottom />
  </footer>
</template>

<script>
import FooterNav from "./FooterNav.vue";
import FooterBottom from "./FooterBottom.vue";
export default {
  name: "FooterComp",
  components: {
    FooterNav,
    FooterBottom,
  },
};
</script>

<style>
footer {
  background-color: #202942;
}
</style>
