<template>
  <section id="footer-top">
    <div class="container w-75 py-5 d-flex flex-column align-items-center">
      <div class="row">
        <!-- left -->
        <div class="col-4 p-3">
          <FooterCard :imgUrl="FooterCardShopImgUrl" />
        </div>
        <!-- center -->
        <div class="col-4 p-3 d-flex align-items-center flex-column">
          <img
            class="img-fluid my-3"
            src="../../assets/img/avadabarbers-logo-x1.png"
            alt="Avada Footer Shop"
          />
          <!-- Contacts -->
          <div class="contacts">
            <span
              v-for="(info, index) in infos"
              :key="index"
              class="text-muted text-center d-block"
              >{{ info }}</span
            >
          </div>

          <!-- Socials -->
          <div class="socials">
            <h5 class="py-5">FOLLOW US</h5>
            <div class="social-icons">
              <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
              <a href="#"><i class="fa-brands fa-twitter"></i></a>
              <a href="#"><i class="fa-brands fa-youtube"></i></a>
              <a href="#"><i class="fa-brands fa-instagram"></i></a>
            </div>
          </div>
        </div>
        <!-- right -->
        <div class="col-4 p-3">
          <FooterCard :imgUrl="FooterCardAppointmentImgUrl" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import FooterCard from "./FooterCard.vue";

export default {
  name: "FooterTop",
  components: { FooterCard },
  props: ["infos", "FooterCardShopImgUrl", "FooterCardAppointmentImgUrl"],
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/_vars.scss";

#footer-top {
  background-color: $cod-gray;
  .socials {
    h5 {
      color: $driftwood;
      font-size: 13px;
      text-align: center;
      letter-spacing: 3px;
      font-weight: bold;
    }
    .social-icons {
      text-align: center;
      a {
        color: $icon-color;
        & * {
          padding: 0 6px;
        }
      }
    }
  }
}
</style>