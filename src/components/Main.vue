<template>
  <main>
    <!-- SECTION JUMBOTRON  -->
    <section id="jumbotron">
      <div class="container">
        <div class="row">
          <Jumbotron />
        </div>
      </div>
    </section>
    <!-- SECTION TRAINING CARDS  -->
    <section class="container">
      <div class="card-container">
        <Cards v-for="(training, index) in trainings" :key="index" :training="training"/>
      </div>
    </section>
    <!-- SECTION QUOTE  -->
     <section id="quote" class="mb-5">
      <div class="container">
        <h1 class="fs-1 text-light text-center">
          "How you respond to the challenge in the second half will determine
          what you become after the game,<br />
          whether you are a winner or a loser."
        </h1>
        <p class="text-center m-3">geroglifico</p>
        <figure class="text-center">
          <img class="rounded-circle" src="../assets/img/avatar-1-2x.jpg" alt="avatar" />
          <span class="m-3 text-light fs-6">Brad Johnson</span>
          <span class="text-grey">Las Vegas</span>
        </figure>
      </div>
    </section>
    <!-- SECTION HERO  -->
    <section id="hero">
        <Hero />   
    </section>
  </main>
</template>

<script>
import Cards from "../components/Cards.vue"
import Hero from "../components/Hero.vue";
import Jumbotron from "../components/Jumbotron.vue";
export default {
  components: { Jumbotron, Hero, Cards },
  name: "Main",
  data() {
    return {
      trainings: [
        {
          title: "Crossfit workout",
          text: "Push your limits",
          img: require("@/assets/img/service6-2x.jpg")
          
        },
        {
          title: "New gym apparel",
          text: "Look good, feel good",
          img: require("@/assets/img/box1-2x.jpg"),
        },
        {
          title: "Team training",
          text: "Find a partner",
          img: require("@/assets/img/box3-2x.jpg"),
        },
      ],
    };
  },
};
</script>   

<style lang="scss">


</style>