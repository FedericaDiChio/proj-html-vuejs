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
      logo: require("@/assets/img/logo.png"),
      menus: [
        {
          text: "Home",
          url: "#",
        },
        {
          text: "Services",
          url: "#",
        },
        {
          text: "About",
          url: "#",
        },
        {
          text: "Videos",
          url: "#",
        },
        {
          text: "Blog",
          url: "#",
        },
        {
          text: "Store",
          url: "#",
        },
         {
          text: "Store",
          url: "#",
        },
      ],
    };
  },
}
</script>

<style lang="scss">
@import "./assets/styles/style.scss";

</style>
