<template>
  <!-- <HelloWorld msg="Hello Vue 3.0 + Vite" :obs="{tes:'te'}" /> -->
  <navbar />
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
};
</script>
