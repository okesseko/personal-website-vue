<template>
  <footer id="contact_">
    <h2 class="main-title">聯絡</h2>
    <div id="contact-methods">
      <p>
        <a href="tel:886-0908661587">
          <img class="contact-img" src="../images/phone-call.svg" />
          <span>09-08661587</span>
        </a>
      </p>
      <p>
        <a href="mailto:okesseko@gmail.com">
          <img class="contact-img" src="../images/gmail.svg" />
          <span>okesseko@gmail.com </span>
        </a>
      </p>
      <p>
        <a href="https://github.com/okesseko">
          <img class="contact-img" src="../images/github.svg" />
          <span>okesseko </span>
        </a>
      </p>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Contact",
};
</script>

<style scoped>
@import "../css/font.css";
@import "../css/image.css";
@import "../css/display.css";
#contact_ {
  width: 100%;
  background: rgba(44, 73, 127, 0.7);
  padding: 2rem 0 4rem 0;
}
a {
  color: black;
  text-decoration: none;
  animation: all 0.3 ease-out 0s;
}
a span {
  padding-bottom: 3px;
  border-bottom: 1px solid;
}
a:hover {
  color: white;
}
</style>
