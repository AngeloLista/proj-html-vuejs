<template>
  <a href="#">{{ text }}</a>
</template>

<script>
export default {
  name: "BottomLink",
  props: ["text"],
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";

a {
  border: 2px solid $driftwood;
  padding: 15px 45px;
  text-decoration: none;
  color: $driftwood;
  text-transform: uppercase;
  font-weight: bold;
  font-size: 18px;
  &:hover {
    color: $driftwood-hover;
    border: 2px solid $driftwood-hover;
  }
}
</style>