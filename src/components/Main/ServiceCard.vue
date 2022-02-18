<template>
  <div class="service-card d-flex align-items-center flex-column">
    <img :src="imgUrl" :alt="name" />
    <h3>{{ name }}</h3>
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
  img {
    margin-bottom: 30px;
    height: 35%;
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