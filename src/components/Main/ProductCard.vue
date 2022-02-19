<template>
  <div class="product-card d-flex align-items-center flex-column">
    <a href="#">
      <img class="img-fluid" :src="imgUrl" :alt="name" />
      <h3>{{ name }}</h3>
      <span class="price">{{ price }}</span>
    </a>
  </div>
</template>

<script>
export default {
  name: "ProductCard",
  props: ["name", "price", "imgUrl"],
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/_vars.scss";

.product-card {
  width: 25%;
  img {
    margin-bottom: 30px;
  }
  a {
    text-decoration: none;
    text-align: center;
    color: $driftwood;
  }
  h3 {
    font-family: $abril;
    color: $driftwood;
    margin-bottom: 15px;
  }
}
</style>