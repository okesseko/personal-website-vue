<template>
  <div id="menu-bar">
    <div class="tag"><p>關於林詠振</p></div>
    <div class="tag"><p>經驗</p></div>
    <div class="tag"><p>聯絡</p></div>
  </div>
</template>

<script>
export default {
  name: "MenuBar",
};
</script>

<style scoped>
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
.tag {
  cursor: pointer;
  margin-right: 5%;
}
p:hover {
  border-bottom: 3px solid white;
  padding-bottom: 5px;
}
</style>
