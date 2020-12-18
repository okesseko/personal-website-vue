<template>
  <navbar :elemetHeight="elemetHeight" />
  <home />
  <about-me />
  <experience />
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
    };
  },
  mounted() {
    this.countHeight();
  },
  methods: {
    countHeight() {
      this.elemetHeight.push(document.getElementById("home_").offsetTop);
      this.elemetHeight.push(document.getElementById("about-me_").offsetTop);
      this.elemetHeight.push(document.getElementById("experience_").offsetTop);
      this.elemetHeight.push(document.getElementById("contact_").offsetTop);
    },
  },
};
</script>
