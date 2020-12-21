<template>
  <transition name="fade">
    <header id="navbar" v-show="navbarShow">
      <button
        id="seeMore"
        v-show="mediaType === 'phone'"
        class="small-icon"
        @click="seeMore = !seeMore"
      />
      <div
        :class="{ backdrop: mediaType === 'phone' }"
        v-show="mediaType === 'phone' ? seeMore : true"
        @touchmove.prevent
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
            <li class="nav-tag" :class="{ color: nowPlace === 'about-me' }">
              <a href="#about-me_" @click="onClick('about-me')">關於林詠振</a>
            </li>
            <li class="nav-tag" :class="{ color: nowPlace === 'experience' }">
              <a href="#experience_" @click="onClick('experience')">經驗</a>
            </li>
            <li class="nav-tag" :class="{ color: nowPlace === 'contact' }">
              <a href="#contact_" @click="onClick('contact')">聯絡</a>
            </li>
          </ul>
        </nav>
      </div>
    </header>
  </transition>
</template>

<script>
export default {
  name: "Navbar",
  props: {
    elemetHeight: {
      default: [],
    },
    scrollH: {
      default: 0,
    },
  },
  data() {
    return {
      navbarShow: false,
      lastScrollY: 0,
      mediaType: "phone",
      seeMore: false,
      nowPlace: "home",
    };
  },
  created() {
    this.onResize();
    window.addEventListener("resize", this.onResize);
  },
  unmounted() {
    window.addEventListener("resize", this.onResize);
  },
  watch: {
    seeMore: function () {
      if (this.seeMore) {
        document.querySelector("body").style.overflow = "hidden";
      } else {
        document.querySelector("body").style.overflow = "scroll";
      }
    },
    scrollH: function () {
      if (this.scrollH <= this.elemetHeight[1]) {
        this.nowPlace = "home";
        location.hash = "home";
      } else if (
        this.elemetHeight[1] < this.scrollH &&
        this.scrollH <= this.elemetHeight[2]
      ) {
        this.nowPlace = "about-me";
        location.hash = "about-me";
      } else if (
        this.elemetHeight[2] < this.scrollH &&
        this.scrollH <= this.elemetHeight[3]
      ) {
        this.nowPlace = "experience";
        location.hash = "experience";
      } else {
        this.nowPlace = "contact";
        location.hash = "contact";
      }
      if (this.scrollH < this.lastScrollY) {
        this.navbarShow = true;
      } else {
        this.navbarShow = false;
      }
      this.lastScrollY = this.scrollH;
    },
  },
  methods: {
    onClick(id) {
      this.seeMore = false;
      this.nowPlace = id;
      console.log(id);
    },
    onResize() {
      if (window.innerWidth >= 768) {
        this.mediaType = "table";
      } else {
        this.mediaType = "phone";
      }
    },
    stopScroll(e) {
      console.log(e);
      e.stopPropagation();
      e.preventDefault();
    },
  },
};
</script>

<style scoped>
@import "../css/font.css";
@import "../css/display.css";
@import "../css/image.css";

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
#navbar {
  width: 100%;
  height: 4rem;
  position: fixed;
  z-index: 1;
}
.color a {
  color: #a9def9;
}
.backdrop {
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
ul {
  list-style: none;
  padding: 0;
}
@media screen and (min-width: 768px) {
  #navbar {
    background: rgba(0, 0, 0, 0.7);
  }
  li {
    display: inline-block;
  }
  .nav-tag {
    padding: 0px 20px;
  }
}
</style>
