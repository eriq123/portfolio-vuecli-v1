<template>
  <b-navbar
    toggleable="lg"
    type="light"
    variant="transparent"
    class="border-bottom"
    id="main-navigation"
  >
    <b-container>
      <b-navbar-brand href="#" class="d-flex">
        <b-navbar-toggle
          target="nav-collapse"
          class="border-0"
        ></b-navbar-toggle>
        <h3 class="mb-0 align-self-center">Eriq John Mendoza</h3>
      </b-navbar-brand>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav
          class="ml-auto text-center"
          v-b-scrollspy:navbar-nav-scroller
        >
          <b-nav-item href="#about" class="mx-3">About</b-nav-item>
          <b-nav-item href="#projects" class="mx-3">Projects</b-nav-item>
          <b-nav-item href="#projects" class="mx-3">Contact</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-container>
  </b-navbar>
</template>
<script>
export default {};
</script>