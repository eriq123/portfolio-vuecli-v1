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
            <b-card
              no-body
              class="overflow-hidden cursor-pointer"
              @click="openModal(project)"
            >
              <b-row no-gutters>
                <b-col md="6" class="d-none d-md-block">
                  <project-card-content
                    :title="project.name | capitalize"
                    :stack="project.stack"
                  >
                    <template v-if="project.description">
                      {{ project.description }}
                    </template>
                  </project-card-content>
                </b-col>
                <b-col md="6">
                  <b-carousel
                    :interval="2000"
                    controls
                    indicators
                    background="#ababab"
                    fade
                  >
                    <b-carousel-slide
                      v-for="(image, index) in project.images"
                      :key="index"
                    >
                      <template #img>
                        <img
                          class="d-block w-100 project-image"
                          width="1024"
                          :src="image.src"
                          :alt="`${modal.title} images`"
                        />
                      </template>
                    </b-carousel-slide>
                  </b-carousel>
                </b-col>
                <b-col md="6" class="d-md-none">
                  <project-card-content
                    :title="project.name | capitalize"
                    :stack="project.stack"
                  >
                    <template v-if="project.description">
                      {{ project.description }}
                    </template>
                  </project-card-content>
                </b-col>
              </b-row>
            </b-card>
          </b-col>
        </b-row>
      </b-container>

      <b-modal
        id="project-modal"
        hide-footer
        centered
        size="xl"
        body-class="p-0"
        :title="modal.title | capitalize"
      >
        <b-carousel
          id="carousel-1"
          :interval="2000"
          controls
          indicators
          background="#ababab"
          fade
          no-hover-pause
        >
          <b-carousel-slide v-for="(image, index) in modal.images" :key="index">
            <template #img>
              <img
                class="d-block w-100 h-480"
                width="1024"
                :src="image.src"
                :alt="`${modal.title} images`"
              />
            </template>
          </b-carousel-slide>
        </b-carousel>
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
          description:
            "This is my first freelance project, an inventory system which was requested by a perfume company Beauty n Bottles. I used bootstrap 3 as my main css framework and laravel as my backend.",
          images: [
            {
              src: `${require("@/assets/projects/beautynbottles-v1/home.png")}`,
            },
            {
              src: `${require("@/assets/projects/beautynbottles-v1/accounts.png")}`,
            },
            {
              src: `${require("@/assets/projects/beautynbottles-v1/category.png")}`,
            },
            {
              src: `${require("@/assets/projects/beautynbottles-v1/convert-stocks.png")}`,
            },
            {
              src: `${require("@/assets/projects/beautynbottles-v1/report.png")}`,
            },
            {
              src: `${require("@/assets/projects/beautynbottles-v1/login.png")}`,
            },
          ],
        },
        {
          show: true,
          name: "BnB Inventory version 2",
          thumbnail: `${require("@/assets/projects/beautynbottles-v2/home.png")}`,
          stack: "Laravel / Vue JS / Vuetify",
          description:
            "This is my latest project which is the same inventory system but with a lot of different functionalities. The main purpose of the second version is to provide a report for easy quarter audit.",
          images: [
            {
              src: `${require("@/assets/projects/beautynbottles-v2/home.png")}`,
            },
            {
              src: `${require("@/assets/projects/beautynbottles-v2/raw.png")}`,
            },
            {
              src: `${require("@/assets/projects/beautynbottles-v2/raw-update.png")}`,
            },
            {
              src: `${require("@/assets/projects/beautynbottles-v2/assembly.png")}`,
            },
            {
              src: `${require("@/assets/projects/beautynbottles-v2/flow.png")}`,
            },
            {
              src: `${require("@/assets/projects/beautynbottles-v2/report.png")}`,
            },
          ],
        },
        {
          show: true,
          name: "Calendar Event",
          thumbnail: `${require("@/assets/projects/appetizer-event-exam/home.png")}`,
          stack: "Laravel / Vue JS",
          description:
            "Calendar event is an application made to easily track events that provides a nice user interface with the help of vue components. This is my first Vue JS application that i submitted to a company as part of the coding examination.",
          images: [
            {
              src: `${require("@/assets/projects/appetizer-event-exam/home.png")}`,
            },
            {
              src: `${require("@/assets/projects/appetizer-event-exam/home-success.png")}`,
            },
            {
              src: `${require("@/assets/projects/appetizer-event-exam/home-with-data.png")}`,
            },
            {
              src: `${require("@/assets/projects/appetizer-event-exam/home-with-data-2.png")}`,
            },
          ],
        },
        {
          show: true,
          name: "Animal Shelter",
          thumbnail: `${require("@/assets/projects/animal-shelter/home.png")}`,
          stack: "Laravel / Bootstrap 5 / SASS",
          description:
            "Animal Shelter is one of my freelance projects which helps a business to monitor rescued animals. It also monitors rescuers, adopters, donations etc. This is quite a small project but it can also help developers who are just starting with laravel since it has a lot of CRUD.",
          images: [
            {
              src: `${require("@/assets/projects/animal-shelter/home.png")}`,
            },
            {
              src: `${require("@/assets/projects/animal-shelter/animals.png")}`,
            },
            {
              src: `${require("@/assets/projects/animal-shelter/animals-read.png")}`,
            },
            {
              src: `${require("@/assets/projects/animal-shelter/animals-add.png")}`,
            },
            {
              src: `${require("@/assets/projects/animal-shelter/rescuers.png")}`,
            },
          ],
        },
        {
          show: true,
          name: "Expense Manager",
          thumbnail: `${require("@/assets/projects/expense-manager/home.png")}`,
          stack: "Laravel / Bootstrap 3 / jQuery",
          description:
            "Expense Manager got me my first job. This is part of a coding examination which consist of atleast 4 CRUD and role based application.",
          images: [
            {
              src: `${require("@/assets/projects/expense-manager/home.png")}`,
            },
            {
              src: `${require("@/assets/projects/expense-manager/category.png")}`,
            },
            {
              src: `${require("@/assets/projects/expense-manager/expenses.png")}`,
            },
            {
              src: `${require("@/assets/projects/expense-manager/roles.png")}`,
            },
            {
              src: `${require("@/assets/projects/expense-manager/users.png")}`,
            },
          ],
        },
      ],
      modal: {
        title: null,
        stack: null,
        images: [],
      },
    };
  },
  components: {
    ProjectCardContent,
  },
  methods: {
    openModal(project) {
      this.modal.description = this.modal.title = this.modal.stack = null;
      this.modal.title = project.name;
      this.modal.stack = project.stack;
      this.modal.images = project.images;
      this.$root.$emit("bv::show::modal", "project-modal");
    },
  },
  filters: {
    capitalize(value) {
      return value ? value.toUpperCase() : "";
    },
  },
};
</script>