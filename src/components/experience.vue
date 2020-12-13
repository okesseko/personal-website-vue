<template>
  <div id="experience">
    <introduce
      title="經驗"
      :des-title="desTitle"
      :content="content"
      :images="images"
    />
  </div>
</template>

<script>
import Introduce from "./introduce.vue";
export default {
  name: "Experience",
  data() {
    return {
      desTitle: ["台灣科技大學 資訊工程系學士班"],
      content: [`專題教授: 戴文凱教授 \n 專題資料...`],
      images: ["TaiwanTech.png"],
    };
  },
  components: { Introduce },
};
</script>

<style >
#experience {
  height: 100%;
  background-color: white;
}
</style>