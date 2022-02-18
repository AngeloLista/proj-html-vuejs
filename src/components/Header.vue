<template>
  <header>
    <!-- header menu -->
    <div
      class="container py-3 d-flex align-items-center justify-content-between"
    >
      <!-- Logo -->
      <img
        src="../assets/img/avadabarbers-logo-x1.png"
        alt="Avada Barbers Logo"
      />
      <!-- Hamburger menu and shop icon -->
      <div class="shop-menu">
        <i class="fa-solid fa-cart-shopping px-3"></i
        ><i class="fa-solid fa-lg fa-bars px-3"></i>
      </div>
    </div>
    <!-- Jumbotron -->
    <div class="jumbotron container">
      <div class="row">
        <div
          class="
            col-6
            d-flex
            justify-content-center
            flex-column
            align-items-start
          "
        >
          <h1>Barber Shop</h1>
          <div class="separator"></div>
          <p>The pinnacle of Male Grooming</p>
          <a href="#">LEARN MORE</a>
        </div>
        <div class="col-6 d-flex flex-column align-items-end">
          <img
            class="img-fluid"
            src="../assets/img/avadabarbers_hero_focalmirror-400x550.png"
            alt="barber jumbotron image"
          />
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";

header {
  background-image: url("../assets/img/avadabarbers-homepage-hero-bg.jpg");
  background-size: cover;
  height: 100vh;
  font-family: $lato;

  .shop-menu {
    color: white;
  }
  .jumbotron {
    color: white;
    padding: 0 30px;
    h1 {
      font-family: $abril;
      font-size: 5rem;
      margin-bottom: 1.3rem;
    }
    .separator {
      height: 3px;
      background-color: $driftwood;
      width: 33%;
      margin-bottom: 1.5rem;
    }
    p {
      font-size: 1.1rem;
      margin-bottom: 1.5rem;
      color: $emperor;
    }
    a {
      border: 2px solid $driftwood;
      padding: 10px 30px;
      text-decoration: none;
      color: $driftwood;
    }
  }
}
</style>