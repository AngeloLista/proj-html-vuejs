<template>
  <div class="section-title">
    <span>{{ description }}</span>
    <h2>{{ title }}</h2>
  </div>
</template>

<script>
export default {
  name: "SectionTitle",
  props: ["title", "description"],
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/_vars.scss";

span {
  color: $driftwood;
  font-weight: bold;
  display: block;
  text-transform: uppercase;
  text-align: center;
}
h2 {
  font-family: $abril;
  font-size: 70px;
  color: $silver-chalice;
  margin-bottom: 1.9rem;
  text-align: center;
}
</style>