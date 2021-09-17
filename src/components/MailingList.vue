<template>
  <div class="col-8">
    <p class="fs-4 text-sienna">{{ mailingLink.text}}</p>
    <h1 class="text-light">{{ mailingLink.title}}</h1>
    <p></p>
    <p class="fs-5 text-grey">
      {{ mailingLink.caption}}
    </p>
    <div class="mt-5 myButtons">
        <input type="text">
        <button class="btn">Subscribe</button>
    </div> 
  </div>

</template>

<script>
export default {
  name: "MailingList",
  props: ["mailingLink"],
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/_mixin.scss";

.btn {
  @include buttons ("blue");
}



</style>

