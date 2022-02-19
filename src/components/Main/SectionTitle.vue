<template>
  <div class="section-title">
    <span>award winning</span>
    <h2>Pro Babers</h2>
  </div>
</template>

<script>
export default {
  name: "SectionTitle",
  props: ["title", "description"],
};
</script>

<style scoped lang="scss">
span {
  color: $driftwood;
  font-weight: bold;
  display: block;
  text-transform: uppercase;
}
h2 {
  font-family: $abril;
  font-size: 70px;
  color: $silver-chalice;
  margin-bottom: 1.9rem;
}
</style>