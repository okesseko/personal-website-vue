<template>
  <header id="navbar" v-show="navbarShow">
    <button
      id="seeMore"
      v-show="mediaType === 'phone'"
      class="small-icon"
      @click="seeMore = !seeMore"
    />
    <div
      :class="{ yy: mediaType === 'phone' }"
      v-show="mediaType === 'phone' ? seeMore : true"
    >
      <button
        id="leave"
        class="small-icon"
        v-show="mediaType === 'phone' ? seeMore : false"
        @click="seeMore = !seeMore"
      />
      <nav
        :class="{
          'flex-center': mediaType === 'phone',
          'flex-end': mediaType !== 'phone',
        }"
        :style="{ height: mediaType === 'phone' ? '100%' : '4rem' }"
      >
        <ul>
          <li class="nav-tag">
            <a
              href="#about-me_"
              :class="{ color: nowPlace === 'about-me' }"
              @click="onClick('about-me')"
              >關於林詠振</a
            >
          </li>
          <li class="nav-tag">
            <a
              href="#experience_"
              :class="{ color: nowPlace === 'experience' }"
              @click="onClick('experience')"
              >經驗</a
            >
          </li>
          <li class="nav-tag">
            <a
              href="#contact_"
              :class="{ color: nowPlace === 'contact' }"
              @click="onClick('contact')"
              >聯絡</a
            >
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "Navbar",
  props: {
    elemetHeight: [],
  },
  data() {
    return {
      navbarShow: false,
      lastScrollY: 0,
      mediaType: "phone",
      seeMore: false,
      isColse: false,
      nowPlace: "home",
    };
  },
  created() {
    this.onResize();
    window.addEventListener("scroll", this.debounce);
    window.addEventListener("resize", this.onResize);
  },
  unmounted() {
    window.removeEventListener("scroll", this.debounce);
    window.addEventListener("resize", this.onResize);
  },
  watch: {
    seeMore: function () {
      if (this.seeMore)
        document.getElementsByTagName("body")[0].style.overflow = "hidden";
      else document.getElementsByTagName("body")[0].style.overflow = "scroll";
    },
  },
  methods: {
    onClick(id) {
      this.seeMore = false;
      this.nowPlace = id;
      console.log(id);
    },
    debounce() {
      if (!this.isColse) {
        this.isColse = true;
        this.handleScroll();
        setTimeout(() => {
          this.isColse = false;
        }, 1000 / 60);
      }
    },
    handleScroll() {
      let now = window.scrollY;
      if (now < this.elemetHeight[1]) {
        this.nowPlace = "home";
        location.hash = "home";
      } else if (this.elemetHeight[1] <= now && now < this.elemetHeight[2]) {
        this.nowPlace = "about-me";
        location.hash = "about-me";
      } else if (this.elemetHeight[2] <= now && now < this.elemetHeight[3]) {
        this.nowPlace = "experience";
        location.hash = "experience";
      } else {
        this.nowPlace = "contact";
        location.hash = "contact";
      }
      if (now < this.lastScrollY) {
        this.navbarShow = true;
      } else {
        this.navbarShow = false;
      }
      this.lastScrollY = now;
    },
    onResize() {
      if (window.innerWidth >= 768) {
        this.mediaType = "table";
      } else {
        this.mediaType = "phone";
      }
    },
  },
};
</script>

<style scoped>
@import "../css/font.css";
@import "../css/display.css";
@import "../css/image.css";
#navbar {
  width: 100%;
  height: 4rem;
  position: fixed;
}
.color {
  color: black;
}
.yy {
  height: 100vh;
  background-color: rgba(0, 0, 0, 0.55);
}
#seeMore {
  border-radius: 100%;
  background-image: url(../images/more.jpg);
}
#leave {
  border-radius: 100%;
  border: 4px solid;
  background-image: url(../images/close.png);
}
.tes {
  width: 100%;
  height: 100%;
}
@media screen and (min-width: 768px) {
  #navbar {
    background: rgba(44, 73, 127, 0.7);
  }
  li {
    display: inline-block;
  }
  .nav-tag {
    padding: 0px 20px;
  }
}
ul {
  list-style: none;
  padding: 0;
}
li,
a {
  text-decoration: none;
  color: white;
}
li a {
  transition: all 0.3s ease 0s;
}
li a:hover {
  color: black;
}
</style>
