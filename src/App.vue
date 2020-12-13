<template>
  <!-- <HelloWorld msg="Hello Vue 3.0 + Vite" :obs="{tes:'te'}" /> -->
  <menu-bar />
  <home />
  <about-me />
  <experience />
</template>

<script>
import AboutMe from "./components/aboutMe.vue";
import Experience from "./components/experience.vue";
import Home from "./components/home.vue";
import MenuBar from "./components/menuBar.vue";
export default {
  name: "App",
  components: { Home, MenuBar, AboutMe, Experience },
};
</script>
