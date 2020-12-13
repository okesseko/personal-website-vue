<template>
  <!-- <HelloWorld msg="Hello Vue 3.0 + Vite" :obs="{tes:'te'}" /> -->
  <menu-bar />
  <main-img />
  <about-me/>
  <experience/>
</template>

<script>
import AboutMe from './components/aboutMe.vue';
import Experience from './components/experience.vue';
import MainImg from "./components/mainImg.vue";
import MenuBar from "./components/menuBar.vue";
export default {
  name: "App",
  components: { MainImg, MenuBar, AboutMe, Experience },
};
</script>
