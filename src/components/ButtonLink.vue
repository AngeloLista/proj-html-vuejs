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
  padding: 10px 30px;
  text-decoration: none;
  color: $driftwood;
  &:hover {
    color: $driftwood-hover;
    border: 2px solid $driftwood-hover;
  }
}
</style>