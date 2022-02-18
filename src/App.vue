<template>
  <div id="app">
    <Header />
    <Main :services="services" />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: { Header, Main, Footer },
  data() {
    return {
      services: [
        {
          name: "Trim & Cut",
          text: "Avada Barbers are experts in the lickety split trim and hair cut. Quick but careful and ridiculously good looking.",
          imgUrl: require("./assets/img/avadabarbers-trimcut-icon-before.png"),
        },
        {
          name: "Wash & Dry",
          text: "Take a seat in our fine leather chairs, lean back and let us lather you a fresh head in a luxurios fascion.",
          imgUrl: require("./assets/img/avadabarbers-washndry-icon.png"),
        },
        {
          name: "Beard Tidy",
          text: "Tame the tangles and untidy facial hairs like a gentleman with our Beard Tidy services from Avada Barbers.",
          imgUrl: require("./assets/img/avadabarbers-beardtrim-icon.png"),
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
</style>