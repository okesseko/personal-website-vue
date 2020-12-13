<template>
  <div id="home" class="home-background grid">
    <h1 class="home-title">
      <i>你好，我是</i> <br />
      <p class="home-subtitle">林詠振</p>
    </h1>
  </div>
</template>

<script>
export default {
  name: "Home",
};
</script>

<style scoped>
@import "../css/font.css";
@import "../css/image.css";
@import "../css/display.css";
#home {
  background-image: url("../images/main.jpg");
  height: 100vh;
  width: 100%;
}
</style>
