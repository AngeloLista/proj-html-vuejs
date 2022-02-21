<template>
  <div>
    <a href="#">
      <img class="img-fluid my-3" :src="imgUrl" alt="Avada Barbers Now Open" />
    </a>
    <a href="#">
      <h3>{{ title }}</h3>
    </a>
    <p class="text-muted text-center">
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Phasellus ut
      dapibus magna. Present semper.
    </p>
  </div>
</template>

<script>
export default {
  name: "BlogPostCard",
  props: ["title", "imgUrl"],
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/_vars.scss";

a {
  text-decoration: none;
}
h3 {
  color: $driftwood;
  font-family: $abril;
  text-align: center;
  margin-bottom: 15px;
}
img:hover {
  filter: brightness(1.1);
  transition: 1s;
}
</style>