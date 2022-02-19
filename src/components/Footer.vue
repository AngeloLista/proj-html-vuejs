<template>
  <footer>
    <!-- Footer Top -->
    <FooterTop />
  </footer>
</template>

<script>
import FooterTop from "./Footer/FooterTop.vue";
export default {
  name: "Footer",
  components: { FooterTop },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";
@import "../assets/scss/_utils.scss";

footer {
  font-family: $lato;
}
</style>