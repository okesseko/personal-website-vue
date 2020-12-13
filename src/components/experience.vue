<template>
  <div id="experience">
    <h2 class="main-title">經驗</h2>
    <div class="grid">
      <div id="dc-project-icon" class="des-icon" />
      <div>
        <p class="des-title">教授專案</p>
        <p class="des-subtitle">拉霸遊戲:</p>
        <p class="des-cont">
          以Phaser為框架，使用TypeScript撰寫的拉霸遊戲。<br />
          是一款以手機為主的 H5，提供給馬來西亞廠商進行上架和營運的博奕類遊戲。<br />在該專案中我主要擔任progammer進行開發，並和
          QA 進行討論改進遊戲。<br /><br />
        </p>
        <p class="des-subtitle">遊戲後台管理系統:</p>
        <p class="des-cont">
          以 React + Material-ui 進行開發。<br />該專案主要提供給遊戲廠商進行管理使用，可及時監控遊戲營運狀況。<br />並可以使用該套系統和後端伺服器溝通，可針對遊戲、玩家、活動等一系列目標進行
          CRUD。<br />該專案中我主要擔任 PM &amp;
          programmer，除了系統撰寫外也管理整個專案進度，定期和教授開會報告進度。<br /><br />
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Experience",
};
</script>

<style scoped>
@import "../css/font.css";
@import "../css/image.css";
@import "../css/display.css";
#dc-project-icon {
  background-image: url(../images/project.png);
  background-color: rgba(177, 229, 242, 0.8);
}
</style>
