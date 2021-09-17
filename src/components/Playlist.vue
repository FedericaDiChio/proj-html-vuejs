<template>
  <div class="card-box">
    <img :src="getImg(playlist.image)" class="img-fluid" alt="playlist" />
    <div class="text-center mt-4 caption">
      <h4>{{ playlist.title }}</h4>
      <p class="text-blue">{{ playlist.text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Playlist",
  props: ["playlist"],
  methods: {
    getImg(path) {
      return require("@/assets/img/" + path);
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/_mixin.scss";
.card-box {
  height: 300px;
  width: 400px;
  position: relative;
  img {
    @include borders;
  }
}

.caption {
  h4 {
    font-size: 18px;
  }
  p {
    font-size: 15px;
  }
}
</style>