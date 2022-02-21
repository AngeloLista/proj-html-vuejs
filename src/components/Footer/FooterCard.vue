<template>
  <div class="d-flex flex-column align-items-center">
    <a href="#">
      <img class="img-fluid my-3" :src="imgUrl" alt="Avada Footer Card" />
    </a>
    <ButtonLinkLittle text="book your appoinment" />
  </div>
</template>

<script>
import ButtonLinkLittle from "./ButtonLinkLittle.vue";

export default {
  name: "FooterCard",
  components: { ButtonLinkLittle },
  props: ["imgUrl"],
};
</script>

<style scoped lang="scss">
</style>