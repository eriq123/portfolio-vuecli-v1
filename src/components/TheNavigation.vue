<template>
  <b-navbar
    toggleable="lg"
    type="dark"
    variant="dark"
    fixed="top"
    class="border-bottom shadow"
    id="main-navigation"
    v-b-scrollspy
  >
    <b-container>
      <b-navbar-brand v-scroll-to="'#app'" to="/" class="d-flex">
        <b-navbar-toggle
          target="nav-collapse"
          class="border-0"
        ></b-navbar-toggle>
        <b-img-lazy
          fluid
          width="60"
          :src="require('@/assets/eriq_logo.png')"
          alt="Eriq John Mendoza Logo"
        ></b-img-lazy>
        <h3 class="ml-1 ml-lg-3 mb-0 align-self-center">Eriq John Mendoza</h3>
      </b-navbar-brand>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="ml-auto text-center mb-3 mb-lg-0">
          <b-nav-item to="#about" v-scroll-to="'#about'" class="mx-3">
            About
          </b-nav-item>
          <b-nav-item to="#projects" v-scroll-to="'#projects'" class="mx-3">
            Projects
          </b-nav-item>
          <b-nav-item to="#contact" v-scroll-to="'#contact'" class="mx-3">
            Contact
          </b-nav-item>
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