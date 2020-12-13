<template>
  <div id="main-img">
    <p><i>你好，我是</i></p>
    <p>林詠振</p>
  </div>
</template>

<script>
export default {
  name: "MainImg",
};
</script>

<style scoped>
#main-img {
  background-image: url("../images/main.jpg");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  height: 100vh;
  width: 100%;
  display: grid;
  place-content: center;
}
p {
  font-size: 40px;
  color: white;
  margin: 0;
}
p:last-child {
    margin-top: 20px;
  font-size: 80px;
}
</style>