<template>
  <div id="app">
    <TheNavigation />
    <div id="main-wrapper">
      <section id="introduction">
        <b-container
          class="h-100 d-flex flex-column align-content-center justify-content-center text-center"
        >
          <b-jumbotron
            bg-variant="transparent"
            text-variant="light"
            header="Hey, I'm Eriq"
            lead="I am a developer and a freelancer."
          >
            <b-button pill variant="light" size="lg">
              View my projects
            </b-button>
          </b-jumbotron>
        </b-container>

        <div class="hint-down">
          <b-icon
            variant="white"
            icon="arrow-down"
            font-scale="4"
            animation="cylon-vertical"
          ></b-icon>
        </div>
      </section>
      <section id="about">
        <b-container>
          <h1 class="text-center section-title">About</h1>

          <b-alert show variant="success">
            This section is under construction.
          </b-alert>
          <b-row cols="1" cols-md="2" id="about-row"> </b-row>
        </b-container>
      </section>
      <section id="projects">
        <h1 class="text-center section-title">Projects</h1>

        <b-container>
          <b-alert show variant="success">
            This section is under construction.
          </b-alert>
          <b-row cols="1" cols-md="2" cols-lg="3"> </b-row>
        </b-container>
      </section>
      <section id="contact">
        <b-container>
          <h1 class="text-center section-title">Contact</h1>

          <b-alert show variant="success">
            This section is under construction.
          </b-alert>
        </b-container>
      </section>
    </div>
  </div>
</template>
<script>
import TheNavigation from "./components/TheNavigation";
export default {
  components: {
    TheNavigation,
  },
};
</script>
<style lang="scss">
@import "assets/css/main.scss";
</style>
