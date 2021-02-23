<template>
  <section id="projects">
    <div class="offset">
      <h1 class="text-center section-title">Projects</h1>

      <b-container>
        <b-alert show variant="danger" v-if="projects.length == 0">
          Oops, it seems that there are no projects here.
        </b-alert>
        <b-row cols="1" v-if="projects.length > 0">
          <b-col
            v-for="project in projects"
            :key="project.name"
            class="project-column"
          >
            <b-card no-body class="overflow-hidden">
              <b-row no-gutters>
                <b-col md="6" class="d-none d-md-block">
                  <project-card-content
                    :title="project.name | capitalize"
                    :stack="project.stack"
                    @open="openModal(project)"
                  />
                </b-col>
                <b-col md="6">
                  <b-card-img
                    :src="project.thumbnail"
                    :alt="project.name"
                    class="rounded-0 project-image"
                  ></b-card-img>
                </b-col>
                <b-col md="6" class="d-md-none">
                  <project-card-content
                    :title="project.name | capitalize"
                    :stack="project.stack"
                    @open="openModal(project)"
                  />
                </b-col>
              </b-row>
            </b-card>
          </b-col>
        </b-row>
      </b-container>

      <b-modal id="project-modal" hide-footer centered :title="modal.title">
        <p class="my-4">A carousel of {{ modal.title }} will be here soon.</p>
      </b-modal>
    </div>
  </section>
</template>
<script>
import ProjectCardContent from "./ProjectCardContent";
export default {
  data() {
    return {
      projects: [
        {
          show: true,
          name: "BnB Inventory version 1",
          thumbnail: `${require("@/assets/projects/beautynbottles-v1/home.png")}`,
          stack: "Laravel / Bootstrap 4",
        },
        {
          show: true,
          name: "BnB Inventory version 2",
          thumbnail: `${require("@/assets/projects/beautynbottles-v2/home.png")}`,
          stack: "Laravel / Vue JS / Vuetify",
        },
        {
          show: true,
          name: "Calendar Event",
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
      modal: {
        title: null,
      },
    };
  },
  components: {
    ProjectCardContent,
  },
  methods: {
    openModal(project) {
      this.modal.title = null;
      this.modal.title = project.name;
      this.$root.$emit("bv::show::modal", "project-modal");
    },
  },
  filters: {
    capitalize(value) {
      return value.toUpperCase();
    },
  },
};
</script>