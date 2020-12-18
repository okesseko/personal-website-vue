<template>
  <navbar :elemetHeight="elemetHeight" :scrollH="scrollH" />
  <home />
  <about-me  :scrollH="scrollH"/>
  <experience  :scrollH="scrollH"/>
  <contact />
</template>

<script>
import AboutMe from "./components/aboutMe.vue";
import Experience from "./components/experience.vue";
import Home from "./components/home.vue";
import Navbar from "./components/navbar.vue";
import Contact from "./components/contact.vue";
export default {
  name: "App",
  components: { Home, Contact, Navbar, AboutMe, Experience },
  data() {
    return {
      elemetHeight: [],
      scrollH: 0,
       isColse: false,
    };
  },
  mounted() {
    window.addEventListener("scroll", this.debounce);
    this.countHeight();
  },
  unmounted() {
    window.addEventListener("scroll", this.debounce);
  },
  methods: {
    debounce() {
      if (!this.isColse) {
        this.isColse = true;
        this.handleScroll();
        setTimeout(() => {
          this.isColse = false;
        }, 1000 / 60);
      }
    },
    handleScroll() {
      this.scrollH = window.scrollY;
    },
    countHeight() {
      this.elemetHeight.push(document.getElementById("home_").offsetTop);
      this.elemetHeight.push(document.getElementById("about-me_").offsetTop);
      this.elemetHeight.push(document.getElementById("experience_").offsetTop);
      this.elemetHeight.push(document.getElementById("contact_").offsetTop);
    },
  },
};
</script>
