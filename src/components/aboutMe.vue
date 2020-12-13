<template>
  <div id="about-me">
    <h2 class="main-title">關於林詠振</h2>
    <div class="grid">
      <div id="ntust-icon" class="des-icon" />
      <div>
        <p class="des-title">台灣科技大學 資訊工程系學士班</p>
        <p class="des-subtitle">專題教授: 戴文凱教授</p>
        <p class="des-cont">專題資料...</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AboutMe",
};
</script>

<style scoped>
@import "../css/font.css";
@import "../css/image.css";
@import "../css/display.css";
#about-me {
  width: 100%;
}
#ntust-icon {
  background-image: url(../images/TaiwanTech.png);
  background-color: rgba(177, 229, 242, 0.8);
}
</style>
