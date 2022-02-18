<template>
  <main>
    <!-- Pro Barbers -->
    <section id="pro-barbers" class="d-flex flex-column align-items-center">
      <!-- Section text -->
      <div class="content text-center">
        <!-- title DA COMPONENTIZZARE -->
        <span>award winning</span>
        <h2>Pro Babers</h2>
        <ButtonLink text="meet your new barber" />
      </div>
      <div class="triangle-separetor"></div>
      <!-- Triangle Sepator -->
    </section>

    <!-- Services -->
    <section id="services" class="d-flex flex-column align-items-center py-5">
      <!-- Title -->
      <span>mens grooming</span>
      <h2>Services</h2>
      <div class="cards-container container d-flex align-items-center">
        <!-- Card -->
        <div class="service-card d-flex align-items-center flex-column">
          <img
            src="../assets/img/avadabarbers-trimcut-icon-before.png"
            alt="trimcut"
          />
          <h3>Trim & Cut</h3>
          <p class="text-muted">
            Avada Barbers are experts in the lickety split trim and hair cut.
            Quick but careful and ridiculously good looking.
          </p>
        </div>
        <div class="service-card d-flex align-items-center flex-column">
          <!-- Card -->
          <img
            src="../assets/img/avadabarbers-washndry-icon.png"
            alt="trimcut"
          />
          <h3>Wash & Dry</h3>
          <p class="text-muted">
            Take a seat in our fine leather chairs, lean back and let us lather
            you a fresh head in a luxurios fascion.
          </p>
        </div>
        <div class="service-card d-flex align-items-center flex-column">
          <!-- Card -->
          <img
            src="../assets/img/avadabarbers-beardtrim-icon.png"
            alt="trimcut"
          />
          <h3>Beard Tidy</h3>
          <p class="text-muted">
            Tame the tangles and untidy facial hairs like a gentleman with our
            Beard Tidy services from Avada Barbers.
          </p>
        </div>
      </div>
      <ButtonLink text="read about our services" />
    </section>
  </main>
</template>

<script>
import ButtonLink from "./ButtonLink.vue";
export default {
  name: "Main",
  components: {
    ButtonLink,
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";
main {
  font-family: $lato;
  #pro-barbers {
    background-image: url("../assets/img/avadabarbers-about-introbackground.jpg");
    background-size: cover;
    .content {
      padding: 100px 0;
      span {
        color: $driftwood;
        font-weight: bold;
        display: block;
        text-transform: uppercase;
      }
      h2 {
        font-family: $abril;
        font-size: 70px;
        color: $silver-chalice;
        margin-bottom: 1.9rem;
      }
    }
    .triangle-separetor {
      width: 0;
      height: 0;
      line-height: 0;
      border-bottom: 100px solid white;
      border-left: 49.39vw solid transparent;
      border-right: 49.39vw solid transparent;
    }
  }
  #services {
    // Title
    span {
      color: $driftwood;
      font-weight: bold;
      display: block;
      text-transform: uppercase;
    }
    h2 {
      font-family: $abril;
      font-size: 70px;
      color: $silver-chalice;
      margin-bottom: 1.9rem;
    }
    // Card
    .cards-container {
      margin-bottom: 50px;
      .service-card {
        height: 300px;
        width: calc(100% / 3);
        padding: 30px 70px;
        img {
          margin-bottom: 30px;
          height: 35%;
        }
        h3 {
          font-family: $abril;
          color: $driftwood;
          margin-bottom: 30px;
        }
        p {
          text-align: center;
        }
      }
    }
  }
}
</style>