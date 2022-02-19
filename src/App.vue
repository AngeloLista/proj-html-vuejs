<template>
  <div id="app">
    <Header />
    <Main :services="services" :products="products" />
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
      products: [
        {
          name: "Brush",
          price: "$15.00",
          imgUrl: require("./assets/img/brush_dark.png"),
        },
        {
          name: "Scissors",
          price: "$85.00",
          imgUrl: require("./assets/img/scissors.png"),
        },
        {
          name: "Hot Oil",
          price: "$15.00",
          imgUrl: require("./assets/img/hot_oil_dark.png"),
        },
        {
          name: "Straight Razor",
          price: "$30.00",
          imgUrl: require("./assets/img/straight_razor_dark.png"),
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
</style>