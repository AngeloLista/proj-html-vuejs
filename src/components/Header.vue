<template>
  <header>
    <!-- header bar -->
    <HeaderBar />
    <!-- Jumbotron -->
    <Jumbotron />
  </header>
</template>

<script>
import HeaderBar from "./Header/HeaderBar.vue";
import Jumbotron from "./Header/Jumbotron.vue";

export default {
  name: "Header",
  components: { HeaderBar, Jumbotron },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";

header {
  background-image: url("../assets/img/avadabarbers-homepage-hero-bg.jpg");
  background-size: cover;
  height: 100vh;
  font-family: $lato;
}
</style>