<template>
  <div class="row gx-0">
    <div class="col-6">
      <div class="box">
      </div>
    </div>
    <div class="col-5 m-5">
      <p class="fs-4 text-blue">Turn up your workouts</p>
      <h1 class="text-dark">The best health & fitness adivce online</h1>
      <img src="../assets/img/unnamed.jpg" alt="logo" class="m-3">
      <p class="fs-5 text-dark">
        Arcu ei facilisi ut quisque placerat nunc habitant. Magna sempre mauris,
        venenatis, leo integer sit pellentesque
      </p>
      <ButtonYouTube class="mt-4"/>
    </div>
  </div>
</template>

<script>
import ButtonYouTube from "../components/ButtonYouTube.vue" 
export default {
  name: "Hero",
  components: { ButtonYouTube },
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/_mixin.scss";

.btn-bl {
  @include buttons ("green");
}

h1 {
  font-size: 55px;
  font-weight: 400;
}

</style>