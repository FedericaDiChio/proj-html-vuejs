<template>
  <div class="col">
    <p class="fs-4 text-sienna">Certified fitness professional</p>
    <h1 class="text-light">Take control of your health</h1>
    <p>geroglifico</p>
    <p class="fs-5 text-grey">
      Curabitur non nulla sit amet nisl tempus convallis quis ac lectus dolor
      sit amet.
    </p>
    <div class="mt-5 myButtons">
        <ButtonYouTube />
        <button class="px-5 py-2">Buy Avada today</button>
    </div> 
  </div>

</template>

<script>
import ButtonYouTube from "../components/ButtonYouTube.vue" 
export default {
  name: "Jumbotron",
  components: { ButtonYouTube },
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/_mixin.scss";

.btn-bl {
  @include buttons ("blue");
}

button {
  @include buttons;
}


</style>

