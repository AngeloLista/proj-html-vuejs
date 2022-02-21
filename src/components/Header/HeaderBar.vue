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
    <Transition name="slide-fade">
      <div
        class="
          menu
          d-flex
          flex-column
          align-items-center
          justify-content-center
        "
        v-if="isMenuVisible"
      >
        <i
          role="button"
          @click="isMenuVisible = false"
          class="fa-solid fa-xmark fa-2x"
        ></i>
        <a
          v-for="(menuItem, index) in menuItems"
          :key="index"
          @click="isMenuVisible = false"
          :href="`#${menuItem.link}`"
          >{{ menuItem.text }}</a
        >
      </div>
    </Transition>
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
  props: ["menuItems"],
  data() {
    return {
      isMenuVisible: false,
    };
  },
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/_vars.scss";

.slide-fade-enter-active {
  transition: all 0.3s ease-out;
}

.slide-fade-leave-active {
  transition: all 0.3s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter,
.slide-fade-leave-to {
  transform: translateX(20px);
  opacity: 0;
}

#header-bar {
  height: 70px;
}
.menu {
  background-color: black;
  color: $silver-chalice;
  position: fixed;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
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
    color: $silver-chalice;
    text-decoration: none;
    font-size: 33px;
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