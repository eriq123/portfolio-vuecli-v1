<template>
  <div id="main-wrapper">
    <Introduction />
    <section id="about">
      <About />
      <Skills />
    </section>
    <Contact />
    <TheFooter />

    <div class="scroll-container" v-if="visible">
      <b-button
        class="scroll-button"
        variant="light"
        to="/"
        v-scroll-to="'#app'"
      >
        <b-icon icon="caret-up-fill" variant="dark" font-scale="2"></b-icon>
      </b-button>
    </div>
  </div>
</template>

<script>
import Introduction from "@/components/Introduction";
import About from "@/components/About";
import Skills from "@/components/Skills";
import Contact from "@/components/Contact";
import TheFooter from "@/components/TheFooter";

export default {
  name: "index",
  components: {
    Introduction,
    About,
    Skills,
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