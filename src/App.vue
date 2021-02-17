<template>
  <div id="app">
    <TheNavigation />
    <div
      id="main-wrapper"
      data-bs-spy="scroll"
      data-bs-target="#main-nav"
      data-bs-offset="0"
      tabindex="0"
    >
      <Introduction />
      <About />
      <Projects />
      <Contact />
      <TheFooter />

      <div class="scroll-container" v-if="visible">
        <div class="scroll-button" v-scroll-to="'#app'">
          <b-icon icon="caret-up-fill" variant="dark" font-scale="2"></b-icon>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import TheNavigation from "./components/TheNavigation";
import Introduction from "./components/Introduction";
import About from "./components/About";
import Projects from "./components/Projects";
import Contact from "./components/Contact";
import TheFooter from "./components/TheFooter";
export default {
  name: "App",
  components: {
    TheNavigation,
    Introduction,
    About,
    Projects,
    Contact,
    TheFooter,
  },
  data() {
    return {
      visible: false,
    };
  },
  mounted: function () {
    window.addEventListener("scroll", this.scrollListener);
  },
  beforeDestroy: function () {
    window.removeEventListener("scroll", this.scrollListener);
  },
  methods: {
    scrollListener: function () {
      this.visible = window.scrollY > 200;
    },
  },
};
</script>
<style lang="scss">
@import "assets/css/main.scss";
</style>
