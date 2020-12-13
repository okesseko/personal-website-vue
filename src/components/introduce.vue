<template>
  <p class="title">{{ title }}</p>
  <div class="introduce-infos" v-for="(image, index) in images">
    <div
      class="introduce-icon"
      :style="{
        backgroundImage: 'url(/src/images/' + image + ')',
      }"
    />
    <p class="introduce-des-title">{{ desTitle[index] }}</p>
    <p class="introduce-des-cont">{{ content[index] }}</p>
  </div>
</template>

<script>
export default {
  name: "Introduce",
  props: {
    title: {
      type: String,
      default: "title",
    },
    desTitle: {
      default: ["title"],
    },
    content: {
      default: ["contnet"],
    },
    images: {
      default: ["Empty"],
    },
  },
};
</script>

<style scoped>
.introduce-infos {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
}
.introduce-icon {
  width: 80%;
  max-width: 320px;
  height: 260px;
  background-color: rgba(177, 229, 242, 0.8);
  background-repeat: no-repeat;
  background-position: center;
  background-size: 80%;
  border-radius: 15%;
}
.introduce-des-title {
  width: 80%;
  text-align: left;
  font-size: 1.2rem;
  font-weight: bold;
  color: #548c2f;
}
.introduce-des-cont {
  white-space: pre-line;
  margin-top: 0%;
  width: 80%;
  text-align: left;
  font-size: 1.2rem;
  line-height: 150%;
}
.title {
  font-size: 2.6rem;
  margin-bottom: 1.5rem;
}
</style>
