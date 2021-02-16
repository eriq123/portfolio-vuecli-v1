<template>
  <b-navbar
    toggleable="lg"
    type="dark"
    variant="dark"
    fixed="top"
    class="border-bottom shadow"
    id="main-navigation"
  >
    <b-container>
      <b-navbar-brand href="#" class="d-flex">
        <b-navbar-toggle
          target="nav-collapse"
          class="border-0"
        ></b-navbar-toggle>
        <b-img-lazy
          fluid
          width="60"
          :src="require('@/assets/eriq_logo.png')"
          alt="Eriq John Mendoza Logo"
          v-scroll-to="'#main-wrapper'"
        ></b-img-lazy>
        <h3 class="ml-3 mb-0 align-self-center" v-scroll-to="'#main-wrapper'">
          Eriq John Mendoza
        </h3>
      </b-navbar-brand>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="ml-auto text-center mb-3 mb-lg-0">
          <b-nav-item href="#about" v-scroll-to="'#about'" class="mx-3"
            >About</b-nav-item
          >
          <!-- <b-nav-item href="#projects" v-scroll-to="'#projects'" class="mx-3"
            >Projects</b-nav-item
          > -->
          <b-nav-item href="#" v-scroll-to="'#contact'" class="mx-3"
            >Contact</b-nav-item
          >
        </b-navbar-nav>
      </b-collapse>
    </b-container>
  </b-navbar>
</template>
<script>
export default {
  name: "TheNavigation",
};
</script>