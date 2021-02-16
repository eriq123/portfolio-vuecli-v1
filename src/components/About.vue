<template>
  <section id="about">
    <div class="glass-background">
      <b-container>
        <h1 class="text-center section-title">About</h1>

        <b-row>
          <b-col cols="12" lg="auto" class="p-3 p-md-1 text-center">
            <b-img-lazy
              fluid
              rounded="circle"
              width="450"
              :src="require('@/assets/eriq.jpg')"
              alt="Photo of Eriq John Mendoza"
            ></b-img-lazy>
          </b-col>
          <b-col class="px-3 text-justify">
            <h2 class="about-description">
              I am a developer that mainly focused in Laravel and Vue JS
              websites.
            </h2>
            <h2 class="about-description">
              I have a deep passion with coding and has a strong commitment
              towards meeting the client's requirement.
            </h2>
            <h2 class="about-description">
              I spent more than a year as a freelancer where I provide
              innovative solutions to clients as well as explore my life as an
              entrepreneur.
            </h2>
            <b-button pill size="lg" class="mt-3 ml-2" variant="outline-primary"
              >Download resume</b-button
            >
          </b-col>
        </b-row>
      </b-container>
    </div>
    <Skills />
  </section>
</template>
<script>
export default {
  name: "About",
  components: {
    Skills: () => import("./Skills"),
  },
  data() {
    return {};
  },
};
</script>