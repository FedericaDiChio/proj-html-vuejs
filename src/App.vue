<template>
  <div id="app">
    <Header :logo="logo" :menus="menus"/>
    <Main />
    <Footer  :footerLink="footerLink"/>
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
@import "./assets/styles/style.scss";

</style>
