<template>
  <section id="projects">
    <div class="offset">
      <h1 class="text-center section-title">Projects</h1>

      <b-container>
        <b-alert show variant="danger" v-if="projects.length == 0">
          Oops, it seems that there are no projects here.
        </b-alert>
        <b-row cols="1" cols-md="2" v-if="projects.length > 0">
          <b-col
            v-for="project in projects"
            :key="project.name"
            class="project-column"
          >
            <b-card
              :img-src="project.thumbnail"
              :img-alt="project.name"
              img-top
              class="project-card"
              v-if="project.show"
              @mouseover="project.show = !project.show"
            >
            </b-card>

            <div
              class="project-hovered"
              v-if="!project.show"
              @mouseleave="project.show = !project.show"
            >
              <div class="project-text">
                <p class="project-name">{{ project.name }}</p>
                <p class="tech-name text-secondary">{{ project.stack }}</p>
              </div>
              <div class="project-button">
                <b-button variant="outline-primary">Learn More</b-button>
              </div>
            </div>
          </b-col>
        </b-row>
      </b-container>
    </div>
  </section>
</template>
<script>
export default {
  data() {
    return {
      projects: [
        {
          show: true,
          name: "Beauty N' Bottles version 1",
          thumbnail: `${require("@/assets/projects/beautynbottles-v1/home.png")}`,
          stack: "Laravel / Bootstrap 4",
        },
        {
          show: true,
          name: "Beauty N' Bottles version 2",
          thumbnail: `${require("@/assets/projects/beautynbottles-v2/home.png")}`,
          stack: "Laravel / Vue JS / Vuetify",
        },
        {
          show: true,
          name: "Calendar Event App",
          thumbnail: `${require("@/assets/projects/appetizer-event-exam/home.png")}`,
          stack: "Laravel / Vue JS",
        },
        {
          show: true,
          name: "Animal Shelter",
          thumbnail: `${require("@/assets/projects/animal-shelter/home.png")}`,
          stack: "Laravel / Bootstrap 5 / SASS",
        },
        {
          show: true,
          name: "Expense Manager",
          thumbnail: `${require("@/assets/projects/expense-manager/home.png")}`,
          stack: "Laravel / jQuery",
        },
      ],
    };
  },
};
</script>