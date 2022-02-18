<template>
  <div class="jumbotron container px-5">
    <div class="row h-100">
      <!-- Jumbotron title and description -->
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
        <ButtonLink text="LEARN MORE" />
      </div>

      <!-- Jumbotron img -->
      <div class="col-6 d-flex flex-column align-items-end h-100">
        <img
          class="img-fluid h-100"
          src="../../assets/img/avadabarbers_hero_focalmirror-600x825.png"
          alt="barber jumbotron image"
        />
      </div>
    </div>
  </div>
</template>

<script>
import ButtonLink from "../ButtonLink.vue";
export default {
  name: "Jumbotron",
  components: {
    ButtonLink,
  },
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/_vars.scss";

.jumbotron {
  color: white;
  padding: 0 30px;
  height: calc(100% - 70px);
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
    &:hover {
      color: $driftwood-hover;
      border: 2px solid $driftwood-hover;
    }
  }
}
</style>