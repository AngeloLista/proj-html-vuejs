<template>
  <main>
    <section id="award-winning" class="d-flex flex-column align-items-center">
      <span>AWARD WINNING</span>
      <h2>Pro Babers</h2>
      <ButtonLink text="meet your new barber" />
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
  #award-winning {
    background-image: url("../assets/img/avadabarbers-about-introbackground.jpg");
    background-size: cover;
    padding: 100px 0;
    span {
      color: $driftwood;
      font-weight: bold;
      display: block;
    }
    h2 {
      font-family: $abril;
      font-size: 70px;
      color: $silver-chalice;
      margin-bottom: 1.9rem;
    }
  }
}
</style>