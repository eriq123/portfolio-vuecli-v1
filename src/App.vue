<template>
  <div id="app">
    <TheNavigation />
    <div id="main-wrapper">
      <Introduction />
      <About />
      <Projects />
      <Contact />
    </div>
  </div>
</template>
<script>
import TheNavigation from "./components/TheNavigation";
import Introduction from "./components/Introduction";
import About from "./components/About";
import Projects from "./components/Projects";
import Contact from "./components/Contact";
export default {
  components: {
    TheNavigation,
    Introduction,
    About,
    Projects,
    Contact,
  },
};
</script>
<style lang="scss">
@import "assets/css/main.scss";
</style>
