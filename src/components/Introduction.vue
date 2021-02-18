<template>
  <section id="introduction">
    <b-container
      class="h-100 d-flex flex-column align-content-center justify-content-center text-center"
    >
      <b-jumbotron
        bg-variant="transparent"
        text-variant="light"
        header="Hey, I'm Eriq"
        lead="Developer and Freelancer"
      >
        <b-button
          pill
          variant="outline-light"
          size="lg"
          to="#about"
          v-scroll-to="'#about'"
        >
          More about me
        </b-button>
      </b-jumbotron>
    </b-container>

    <div class="hint-down">
      <b-button
        variant="transparent"
        to="#about"
        v-scroll-to="'#about'"
        class="p-0"
      >
        <b-icon
          class="hint-down-icon"
          variant="white"
          icon="chevron-down"
          font-scale="4"
          animation="fade"
        ></b-icon>
      </b-button>
    </div>
  </section>
</template>
<script>
export default {
  name: "Introduction",
};
</script>