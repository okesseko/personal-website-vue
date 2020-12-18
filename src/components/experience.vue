<template>
  <div id="experience_">
    <h2 class="main-title">經驗</h2>
    <div class="grid">
      <div id="dr-project-icon" class="des-icon" />
      <div>
        <p class="des-title">教授專案 <br /><span>2019-12-05 ~ now</span></p>
        <p class="des-subtitle">拉霸遊戲:<br /><span>2019-12-05 ~ 2020-05-31</span></p>
        <p class="des-cont">
          以Phaser為框架，使用TypeScript撰寫的拉霸遊戲。<br />
          是一款以手機為主的 H5，提供給馬來西亞廠商進行上架和營運的博奕類遊戲。<br />在該專案中我主要擔任progammer進行開發，並和
          QA 進行討論改進遊戲。<br /><br />
        </p>
        <p class="des-subtitle">遊戲後台管理系統:<br /><span>2020-10-01 ~ now</span></p>
        <p class="des-cont">
          以 React + Material-ui + Echart 進行開發。<br />該專案主要提供給遊戲廠商進行管理使用，可及時監控遊戲營運狀況。<br />並可以使用該套系統和後端伺服器溝通，可針對遊戲、玩家、活動等一系列目標進行
          CRUD。<br />該專案中我主要擔任 PM &amp;
          programmer，除了系統撰寫外也管理整個專案進度，定期和教授開會報告進度。<br /><br />
        </p>
      </div>
    </div>
    <div class="grid">
      <div id="intern-icon" class="des-icon" />
      <div>
        <p class="des-title">暑期實習 AIG<br /><span>2020-6-25 ~ 2020-9-15</span></p>
        <p class="des-subtitle">
          遊戲後台管理系統:<br /><span>2020-06-25 ~ 2020-9-15</span>
        </p>
        <p class="des-cont">
          以 React + Antd + Rechart 進行開發。<br />
          此專案也是提供給遊戲廠商進行管理，和教授專案的管理系統相似，不過使用不同的元件庫和圖表繪製library。<br />
          該專案中我主要programmer，這是我第一次進行大系統開發，和前輩們學習許多。<br /><br />
        </p>
        <p class="des-subtitle">遊戲介紹網頁:<br /><span>2020-07-20 ~ 2020-8-31</span></p>
        <p class="des-cont">
          以 React + Gatsby 進行開發。<br />此專案是提供給其他合作廠商使用的遊戲介紹網站，可以根據資料庫及時更新網站資訊，提供各遊戲細節以及試玩網站。<br />
          並且提供 RWD 和 PWA
          功能，能夠自動適應所有裝置，並在新遊戲上市時自動進行訊息推波。<br />
          該專案中我主要擔任 PM &amp; programmer，這是我第一次接觸 PWA
          以及不使用任何元件庫撰寫網頁，其中翻閱許多資料以及和前輩們討論。<br /><br />
        </p>
      </div>
    </div>
    <div class="grid">
      <div id="self-project-icon" class="des-icon" />
      <div>
        <p class="des-title">個人專案<br /><span>2020-12-01 ~ now</span></p>
        <p class="des-subtitle">個人網站:<br /><span>2020-12-01 ~ 2020-12-15</span></p>
        <p class="des-cont">
          以 Vue3 進行開發。<br />
          該專案是我第一次使用 Vue 語言，先前專案都是使用 React。<br />
          在研究其特有的語法花費許多時間，也特別不使用任何元件庫，來鍛鍊基本的網頁撰寫。<br />
          該網站參考了許多個人網站，參考最多的是
          <a href="http://www.garysheng.com/">GARY SHENG</a> 的個人網站<br /><br />
          <button @click="openTab">更多資料</button>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Experience",
  methods: {
    openTab() {
      console.log("open");
      window.open("https://github.com/okesseko/personal-website-vue");
    },
  },
};
</script>

<style scoped>
@import "../css/font.css";
@import "../css/image.css";
@import "../css/display.css";
#experience_{
  padding: 2rem 0;
}
#dr-project-icon {
  background-image: url(../images/project.png);
  background-color:  rgba(61, 71, 82);
}
#intern-icon {
  background-image: url(../images/project.png);
  background-color:   rgba(61, 71, 82);
}
#self-project-icon {
  background-image: url(../images/self_project.jpg);
  background-color:  rgba(94, 180, 231);
}
.des-cont a {
    animation: all 0.5s ease-out 0s;
  color: #8c8a93;
}
.des-cont a:hover {
  color: #605e68;
}
.des-cont button {
  border: none;
  border-radius: 44px;
  width: 150px;
  height: 44px;
  background-color: #548c2f;
  color: white;
  cursor: pointer;
  animation: all 0.5s ease-out 0s;
}
.des-cont button:hover {
   background-color: #457425;
}
</style>
