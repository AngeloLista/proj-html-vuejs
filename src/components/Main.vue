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
        <ServiceCard
          v-for="(service, index) in services"
          :key="index"
          :name="service.name"
          :text="service.text"
          :imgUrl="service.imgUrl"
        />
      </div>
      <ButtonLink text="read about our services" />
    </section>
  </main>
</template>

<script>
import ButtonLink from "./ButtonLink.vue";
import ServiceCard from "./Main/ServiceCard.vue";

export default {
  name: "Main",
  components: {
    ButtonLink,
    ServiceCard,
  },
  props: ["services"],
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