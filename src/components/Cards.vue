<template>
<div class="px-3 card-box">
  <img :src="getImg(training.img)" class="img-fluid" alt="training">
  <!-- <div class="caption">
    <h4 class="text-white">{{ training.title }}</h4>
    <p class="card-text">{{ training.text }}</p>
  </div> -->
</div>

    
</template>

<script>
export default {
    name: "Cards",
    props: ["training"],
      methods: {
      getImg(path){
          return require ("@/assets/img/" + path);
      }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/styles/_mixin.scss";
        .card-box {        
            height: 250px;
            width: 350px;
            img {
              @include borders;
              // position: relative; 
            }
        }

        // .caption {
        //   position: absolute;
        //   bottom: 0px;
        //   margin-left: 30px;
          
        // }
</style>