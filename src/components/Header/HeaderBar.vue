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
    <div
      class="menu d-flex flex-column align-items-center justify-content-center"
      v-if="isMenuVisible"
    >
      <i
        role="button"
        @click="isMenuVisible = false"
        class="fa-solid fa-xmark fa-2x"
      ></i>
      <a @click="isMenuVisible = false" href="#services"> Services</a>
      <a @click="isMenuVisible = false" href="#products">Products</a>
      <a @click="isMenuVisible = false" href="#featured">Featured</a>
      <a @click="isMenuVisible = false" href="#reviews">Reviews</a>
      <a @click="isMenuVisible = false" href="#blog">Recent Blog Posts</a>
    </div>
    <div class="shop-menu">
      <a href="#" class="mx-3">
        <i class="fa-solid fa-cart-shopping"></i>
      </a>
      <!-- Hamburger Menu Button -->
      <i
        role="button"
        @click="isMenuVisible = true"
        class="fa-solid fa-lg fa-bars"
      ></i>
    </div>
  </div>
</template>

<script>
export default {
  name: "HeaderBar",
  data() {
    return {
      isMenuVisible: false,
    };
  },
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/_vars.scss";

#header-bar {
  height: 70px;
}
.menu {
  background-color: black;
  color: white;
  position: fixed;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  text-align: center;
  i {
    position: absolute;
    top: 30px;
    right: 30px;
    &:hover {
      color: $driftwood;
      transition: 0.3s;
    }
  }
  a {
    color: white;
    text-decoration: none;
    font-size: 3rem;
    margin-bottom: 30px;
    &:hover {
      color: $driftwood;
      transition: 0.3s;
    }
  }
}
.shop-menu {
  a {
    color: white;

    &:hover {
      color: $driftwood;
      transition: 0.5s;
    }
  }
  i {
    color: white;

    &:hover {
      color: $driftwood;
      transition: 0.5s;
    }
  }
}
</style>