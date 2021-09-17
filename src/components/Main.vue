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
        <Cards
          v-for="(training, index) in trainings"
          :key="index"
          :training="training"
        />
      </div>
    </section>
    <!-- SECTION QUOTE  -->
    <section id="quote" class="mb-5">
      <div class="container">
        <JumboQuote />
      </div>
    </section>
    <!-- SECTION HERO  -->
    <section id="hero">
      <Hero />
    </section>
    <!-- SECTION PLAYLIST  -->
    <section id="playlist">
      <div class="container">
        <div class="row">
          <div class="col mb-4 d-flex justify-content-between">
            <h4>Featured Playlist</h4>
            <p>View all videos</p>
          </div>
        </div>
        <div class="row">
          <div class="col d-flex  justify-content-between">
            <Playlist
              v-for="(playlist, index) in playlists"
              :key="index"
              :playlist="playlist"
            />
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import Jumbotron from "../components/Jumbotron.vue";
import Cards from "../components/Cards.vue";
import JumboQuote from "../components/JumboQuote.vue";
import Hero from "../components/Hero.vue";
import Playlist from "../components/Playlist.vue";
export default {
  components: { Jumbotron,  Cards, JumboQuote, Hero, Playlist, },
  name: "Main",
  data() {
    return {
      trainings: [
        {
          title: "Crossfit workout",
          text: "Push your limits",
          img: "service6-2x.jpg",
        },
        {
          title: "New gym apparel",
          text: "Look good, feel good",
          img: "box1-2x.jpg",
        },
        {
          title: "Team training",
          text: "Find a partner",
          img: "box3-2x.jpg",
        },
      ],
      playlists: [
        {
          title: "Thighs & glute workout",
          text: "Increase your mobility",
          image: "video2-2x.jpg",
        },
        {
          title: "Lift, firm & perk up",
          text: "Feel young again",
          image: "video7-2x.jpg",
        },
        {
          title: "Slim & trim your waist",
          text: "Shed those extra pounds",
          image: "video9-2x.jpg",
        },
      ],
    };
  },
};
</script>   

<style lang="scss">
</style>