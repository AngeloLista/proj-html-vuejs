<template>
  <div
    id="header-bar"
    class="
      container
      px-5
      pt-5
      d-flex
      align-items-center
      justify-content-between
    "
  >
    <!-- Logo -->
    <a href="#">
      <img
        src="../../assets/img/avadabarbers-logo-x1.png"
        alt="Avada Barbers Logo"
      />
    </a>
    <!-- Hamburger menu and shop icon -->
    <div class="shop-menu">
      <a href="#" class="mx-3">
        <i class="fa-solid fa-cart-shopping"></i>
      </a>
      <a href="#" class="mx-3"><i class="fa-solid fa-lg fa-bars"></i></a>
    </div>
  </div>
</template>

<script>
export default {
  name: "HeaderBar",
};
</script>

<style scoped lang="scss">
#header-bar {
  height: 70px;
}
.shop-menu {
  a {
    color: white;
  }
}
</style>