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
            class="p-3 project-column"
          >
            <b-card
              :title="project.name"
              :img-src="project.thumbnail"
              :img-alt="project.name"
              img-top
            >
            </b-card>
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
          name: "Beauty N' Bottles version 1",
          thumbnail: `${require("@/assets/projects/beautynbottles-v1/home.png")}`,
        },
        {
          name: "Beauty N' Bottles version 2",
          thumbnail: `${require("@/assets/projects/beautynbottles-v2/home.png")}`,
        },
        {
          name: "Calendar Event App",
          thumbnail: `${require("@/assets/projects/appetizer-event-exam/home.png")}`,
        },
        {
          name: "Animal Shelter",
          thumbnail: `${require("@/assets/projects/animal-shelter/home.png")}`,
        },
        {
          name: "Expense Manager",
          thumbnail: `${require("@/assets/projects/expense-manager/home.png")}`,
        },
      ],
    };
  },
};
</script>