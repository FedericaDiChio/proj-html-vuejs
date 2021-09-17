<template>
  <div>
    <h1 class="fs-1 text-light text-center">
      {{ quote.text }}
    </h1>
    <p class="text-center m-3"></p>
    <figure class="text-center pt-3">
      <img
        class="rounded-circle"
        :src="getImg(quote.avatar)"
        alt="avatar"
      />
      <span class="m-3 text-light fs-6">{{ quote.author }}</span>
      <span class="text-grey">{{ quote.place }}</span>
    </figure>
  </div>
</template>

<script>
export default {
    name: "JumboQuote",
    props: ["quote"],
    methods: {
    getImg(path) {
      return require("@/assets/img/" + path);
    },
  },
};
</script>

<style>
</style>