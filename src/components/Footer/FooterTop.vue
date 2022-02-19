<template>
  <section id="footer-top">
    <div class="container w-75 py-5 d-flex flex-column align-items-center">
      <div class="row">
        <!-- left -->
        <div class="col-4 p-3 d-flex align-items-center flex-column">
          <a href="#">
            <img
              class="img-fluid my-3"
              src="../../assets/img/avadabarbers_footer_shop_image.png"
              alt="Avada Footer Shop"
            />
          </a>
          <ButtonLink text="shop our range now" />
        </div>
        <!-- center -->
        <div class="col-4 p-3 d-flex align-items-center flex-column">
          <a href="#">
            <img
              class="img-fluid my-3"
              src="../../assets/img/avadabarbers-logo-x1.png"
              alt="Avada Footer Shop"
            />
          </a>
          <!-- Contacts -->
          <div class="contacts">
            <span class="text-muted text-center d-block">Avada Barbers</span
            ><span class="text-muted text-center d-block"
              >123 New York Street</span
            ><span class="text-muted text-center d-block">New York City</span
            ><span class="text-muted text-center d-block"
              >info@yourwebsite.com</span
            ><span class="text-muted text-center d-block"
              >+1 (555) 555-1212</span
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
        <div class="col-4 p-3 d-flex align-items-center flex-column">
          <a href="#">
            <img
              class="img-fluid my-3"
              src="../../assets/img/avadabarbers_footer_appointment_image.png"
              alt="Avada Footer Shop"
            />
          </a>
          <ButtonLink text="book your appoinment" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import ButtonLink from "../ButtonLink.vue";

export default {
  name: "FooterTop",
  components: { ButtonLink },
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
        color: white;
        & * {
          padding: 0 6px;
        }
      }
    }
  }
}
</style>