<template>
  <main>
    <!-- SECTION JUMBOTRON  -->
    <section id="jumbotron">
      <div class="container">
        <div class="row">
          <Jumbotron
            v-for="(jumboLink, index) in jumboLinks"
            :key="index"
            :jumboLink="jumboLink"
          />
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
        <JumboQuote v-for="(quote, index) in quotes" :key="index" :quote="quote" />
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
            <p>View all videos <i class="fas fa-chevron-right"></i></p>
          </div>
        </div>
        <div class="row">
          <div class="col d-flex justify-content-between">
            <Playlist
              v-for="(playlist, index) in playlists"
              :key="index"
              :playlist="playlist"
            />
          </div>
        </div>
      </div>
    </section>
    <!-- SECTION MAILING LIST  -->
    <section id="mailing-list">
      <div class="container">
        <MailingList
          v-for="(mailingLink, index) in mailingLinks"
          :key="index"
          :mailingLink="mailingLink"
        />
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
import MailingList from "../components/MailingList.vue";
export default {
  components: { Jumbotron, Cards, JumboQuote, Hero, Playlist, MailingList },
  name: "Main",
  data() {
    return {
      quotes: [
        {
        text: "How you respond to the challenge in the second half will determine what you become after the game, whether you are a winner or a loser.",
        author: "Brad Johnson",
        place: "Las Vegas",
        avatar: "avatar-1-2x.jpg",
        },
      ],
      jumboLinks: [
        {
        text: "Certified fitness professional",
        title: "Take control of your health",
        logo: "",
        caption:
          "Curabitur non nulla sit amet nisl tempus convallis quis ac lectus dolor sit amet.",
        }
      ],
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
      mailingLinks: [
        {
          text: "Join our mailing list today",
          title: "Insider offer & flash sales in your inbox every week.",
          logo: "",
          caption:
            "Curabitur non nulla sit amet tempus convallis quis act lectus          dolor sit amet, consectetur adipiscing elit sed porttitor lectus.",
        },
      ],
    };
  },
};
</script>   

<style lang="scss">
</style>