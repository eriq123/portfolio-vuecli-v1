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
        <b-button pill variant="outline-light" size="lg" v-scroll-to="'#about'">
          More about me
        </b-button>
      </b-jumbotron>
    </b-container>

    <div class="hint-down">
      <b-icon
        class="hint-down-icon"
        variant="white"
        icon="chevron-down"
        font-scale="4"
        animation="fade"
        v-scroll-to="'#about'"
      ></b-icon>
    </div>
  </section>
</template>
<script>
export default {
  name: "Introduction",
};
</script>