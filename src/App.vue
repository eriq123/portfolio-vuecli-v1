<template>
  <div id="app">
    <TheNavigation />
    <div
      id="main-wrapper"
      data-bs-spy="scroll"
      data-bs-target="#main-navigation"
      data-bs-offset="0"
      tabindex="0"
    >
      <Introduction />
      <About />
      <!-- <Projects /> -->
      <Contact />
      <TheFooter />
    </div>
  </div>
</template>
<script>
import TheNavigation from "./components/TheNavigation";
import Introduction from "./components/Introduction";
import About from "./components/About";
// import Projects from "./components/Projects";
import Contact from "./components/Contact";
import TheFooter from "./components/TheFooter";
export default {
  name: "App",
  components: {
    TheNavigation,
    Introduction,
    About,
    // Projects,
    Contact,
    TheFooter,
  },
};
</script>
<style lang="scss">
@import "assets/css/main.scss";
</style>
