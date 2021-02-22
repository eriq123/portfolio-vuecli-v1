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
                <b-col md="6">
                  <b-card-body :title="project.name">
                    <p class="card-subtitle text-secondary">
                      {{ project.stack }}
                    </p>
                    <p class="card-description">
                      Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                      Veritatis fuga omnis quos dicta voluptatibus quas in
                      cumque, magnam blanditiis reiciendis cum, incidunt
                      consequatur eos quidem sunt illo pariatur consequuntur
                      odit?
                    </p>
                    <div class="text-center">
                      <b-button variant="outline-primary">
                        Learn more
                      </b-button>
                    </div>
                  </b-card-body>
                </b-col>
                <b-col md="6">
                  <b-card-img
                    :src="project.thumbnail"
                    :alt="project.name"
                    class="rounded-0 project-image"
                  ></b-card-img>
                </b-col>
              </b-row>
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