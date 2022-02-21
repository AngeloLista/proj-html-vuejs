<template>
  <div class="service-card d-flex align-items-center flex-column">
    <a id="img-link" href="#"><img :src="imgUrl" :alt="name" /></a>
    <a href="#">
      <h3>{{ name }}</h3>
    </a>
    <p class="text-muted">
      {{ text }}
    </p>
  </div>
</template>

<script>
export default {
  name: "ServiceCard",
  props: ["name", "text", "imgUrl"],
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/_vars.scss";

.service-card {
  height: 300px;
  width: calc(100% / 3);
  padding: 30px 70px;
  #img-link {
    height: 35%;
    margin-bottom: 30px;
  }
  a {
    text-decoration: none;
  }
  img {
    height: 100%;
  }
  h3 {
    font-family: $abril;
    color: $driftwood;
    margin-bottom: 30px;
  }
  p {
    text-align: center;
  }
}
</style>