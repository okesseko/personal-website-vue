<template>
  <div id="about-me_">
    <h2 class="main-title">關於林詠振</h2>

    <transition name="fade" >
      <div  class="grid">
        <div id="ntust-icon" class="des-icon" />
        <div>
          <p class="des-title">台灣科技大學 資訊工程系學士班</p>
          <p class="des-subtitle">專題教授: 戴文凱教授</p>
          <p class="des-cont">專題資料...</p>
        </div>
      </div>
    </transition>
    <!-- <transition name="fade">
      <div v-if="show" class="grid">
        <div id="ntust-icon" class="des-icon" />
        <div>
          <p class="des-title">台灣科技大學 資訊工程系學士班</p>
          <p class="des-subtitle">專題教授: 戴文凱教授</p>
          <p class="des-cont">專題資料...</p>
        </div>
      </div>
    </transition> -->
  </div>
</template>

<script>
export default {
  name: "AboutMe",
  data() {
    return {
      show: true,
    };
  },
  created() {
    // window.addEventListener("scroll", function te(e) {
    //   let ww = document.getElementById("experience");
    //   console.log(ww.offsetTop, this.window.innerHeight + this.window.scrollY);
    // });
  },
};
</script>

<style scoped>
@import "../css/font.css";
@import "../css/image.css";
@import "../css/display.css";
.fade-enter-active,
.fade-leave-active {
  transition: all 5s ease;
}
.fade-enter-from,
.fade-leave-to {
  transform: translateY(20px);
  opacity: 0;
}
#about-me_ {
  padding: 2rem 0;
}
#ntust-icon {
  background-image: url(../images/TaiwanTech.png);
  background-color: rgba(31, 105, 243, 0.199);
}
</style>
