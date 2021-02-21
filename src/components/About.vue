<template>
  <div class="glass-background offset">
    <b-container>
      <h1 class="text-center section-title">About</h1>

      <b-row>
        <b-col cols="12" lg="auto" class="p-3 p-md-1 text-center">
          <b-img-lazy
            fluid
            rounded="circle"
            width="250"
            :src="require('@/assets/eriq.jpg')"
            alt="Photo of Eriq John Mendoza"
          ></b-img-lazy>
        </b-col>
        <b-col class="px-3 text-justify">
          <h2 class="about-description">
            I am a developer that mainly focused on Laravel and Vue JS websites.
          </h2>
          <h2 class="about-description">
            I have a deep passion for coding and has a strong commitment to
            meeting the client's requirement.
          </h2>
          <h2 class="about-description">
            I spent more than a year as a freelancer where I provide innovative
            solutions to clients as well as explore my life as an entrepreneur.
          </h2>
          <a
            href="/files/CV_MENDOZA_20210220.pdf"
            download="cv_mendoza.pdf"
            role="button"
            class="btn mt-3 ml-2 btn-outline-primary btn-lg"
          >
            <b-icon icon="download" class="mr-1"></b-icon>
            Resume
          </a>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script>
export default {
  name: "About",
  components: {},
};
</script>