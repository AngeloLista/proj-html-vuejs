<template>
  <footer>
    <!-- Footer Top -->
    <FooterTop />
    <section id="footer-bottom">
      <p class="text-center">
        Copyright 2012 - 2020 | Avada Theme by ThemeFusion | All Rights Reserved
        | Powered by WordPress
      </p>
    </section>
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
  #footer-bottom {
    height: 70px;
    background-color: $median-cod-gray;
    p {
      line-height: 70px;
      color: $mine-shaft;
    }
  }
}
</style>