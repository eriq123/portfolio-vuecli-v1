<template>
  <section id="skills">
    <b-container>
      <h1 class="text-center section-title">Skills</h1>
      <b-row class="about-row" cols="2" cols-lg="3">
        <b-col
          class="p-3 skills-column"
          v-for="(image, index) in images"
          :key="index"
        >
          <img :src="image.src" :width="image.width" :alt="image.alt" />
        </b-col>
      </b-row>
    </b-container>
  </section>
</template>
<script>
export default {
  name: "Skills",
  data() {
    return {
      images: [
        {
          src: `${require("../assets/icons/php-2.png")}`,
          width: "150",
          alt: "php icon",
        },
        {
          src: `${require("../assets/icons/javascript-3.png")}`,
          width: "100",
          alt: "javascript icon",
        },
        {
          src: `${require("../assets/icons/css3.png")}`,
          width: "100",
          alt: "css3 icon",
        },
        {
          src: `${require("../assets/icons/laravel.png")}`,
          width: "100",
          alt: "laravel icon",
        },
        {
          src: `${require("../assets/icons/jquery.png")}`,
          width: "150",
          alt: "jquery icon",
        },
        {
          src: `${require("../assets/icons/sass.png")}`,
          width: "100",
          alt: "sass icon",
        },
        {
          src: `${require("../assets/icons/vue.png")}`,
          width: "100",
          alt: "vue icon",
        },
      ],
    };
  },
};
</script>