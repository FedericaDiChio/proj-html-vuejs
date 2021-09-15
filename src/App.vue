<template>
  <div id="app">
    <Header :logo="logo" :menus="menus"/>
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  },
  data() {
    return {
      logo: require("@/assets/logo.png"),
      menus: [
        {
          text: "Home",
          url: "#",
          current: true,
        },
        {
          text: "Services",
          url: "#",
          current: false,
        },
        {
          text: "About",
          url: "#",
          current: false,
        },
        {
          text: "Videos",
          url: "#",
          current: false,
        },
        {
          text: "Blog",
          url: "#",
          current: false,
        },
        {
          text: "Store",
          url: "#",
          current: false,
        },
      ],
    };
  },
}
</script>

<style lang="scss">
@import "/styles/style.scss";

</style>
