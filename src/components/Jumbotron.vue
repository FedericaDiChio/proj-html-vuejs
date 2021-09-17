<template>
  <div class="col-8">
    <p class="fs-4 text-sienna">{{ jumboLink.text }}</p>
    <h1 class="text-light">{{ jumboLink.title }}</h1>
    <p></p>
    <p class="fs-5 text-grey">
      {{ jumboLink.caption }}
    </p>
    <div class="mt-5 myButtons">
      <ButtonYouTube />
      <button class="px-5 py-2">Buy Avada today</button>
    </div>
  </div>
</template>

<script>
import ButtonYouTube from "../components/ButtonYouTube.vue";
export default {
  name: "Jumbotron",
  components: { ButtonYouTube },
  props: ["jumboLink"],
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/_mixin.scss";

.btn-bl {
  @include buttons("blue");
}

button {
  @include buttons;
}
</style>

