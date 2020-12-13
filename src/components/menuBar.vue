<template>
  <div id="menu-bar">
    <p class='menu-tag'>關於林詠振</p>
    <p class='menu-tag'>經驗</p>
    <p class='menu-tag'>聯絡</p>
  </div>
</template>

<script>
export default {
  name: "MenuBar",
};
</script>

<style scoped>
@import "../css/font.css";
#menu-bar {
  width: 100%;
  height: 4rem;
  background: rgba(44, 73, 127, 0.7);
  position: fixed;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  font-size: 1.2rem;
  font-weight: bold;
  color: white;
}
</style>
