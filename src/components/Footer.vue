<template>
  <footer>
    <!-- Footer Top -->
    <FooterTop
      :infos="infos"
      :FooterCardShopImgUrl="FooterCardShopImgUrl"
      :FooterCardAppointmentImgUrl="FooterCardAppointmentImgUrl"
    />
    <section id="footer-bottom">
      <p class="text-center">
        &copy; Copyright 2012 - 2020 | Avada Theme by ThemeFusion | All Rights
        Reserved | Powered by WordPress
      </p>
    </section>
  </footer>
</template>

<script>
import FooterTop from "./Footer/FooterTop.vue";
export default {
  name: "Footer",
  components: { FooterTop },
  props: ["infos", "FooterCardShopImgUrl", "FooterCardAppointmentImgUrl"],
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
      font-size: 13px;
    }
    a {
      font-size: 14px;
    }
  }
}
</style>