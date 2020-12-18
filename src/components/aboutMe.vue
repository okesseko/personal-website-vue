<template>
  <div id="about-me_">
    <h2 class="main-title">關於林詠振</h2>

    <div
      id="ntust-des"
      class="grid"
      style="opacity: 0"
      :class="{ fadeIn: show }"
    >
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
  props: {
    scrollH: {
      default: 0,
    },
  },
  data() {
    return {
      show: false,
      eleHeight: 0,
    };
  },
  mounted() {
    this.eleHeight = document.getElementById("ntust-des").offsetTop;
  },
  watch: {
    scrollH: function () {
      if (this.scrollH + window.innerHeight > this.eleHeight) this.show = true;
    },
  },
};
</script>

<style scoped>
@import "../css/font.css";
@import "../css/image.css";
@import "../css/display.css";
#about-me_ {
  padding: 2rem 0;
}
#ntust-icon {
  background-image: url(../images/TaiwanTech.png);
  background-color: rgba(31, 105, 243, 0.199);
}
</style>
