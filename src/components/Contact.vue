<template>
  <section id="contact">
    <div class="offset">
      <b-container>
        <h1 class="text-center section-title text-white">Contact</h1>

        <form action="" id="contact-form" class="glass-background">
          <b-form-group label="First Name:" label-for="first_name" class="mb-3">
            <b-form-input
              type="text"
              id="first_name"
              name="first_name"
              placeholder="First Name"
              required
            ></b-form-input>
          </b-form-group>
          <b-form-group label="Last Name:" label-for="last_name" class="mb-3">
            <b-form-input
              type="text"
              id="last_name"
              name="last_name"
              placeholder="Last Name"
              required
            ></b-form-input>
          </b-form-group>
          <b-form-group label="Email address:" label-for="email" class="mb-3">
            <b-form-input
              type="email"
              id="email"
              name="email"
              placeholder="Email address"
              required
            ></b-form-input>
          </b-form-group>
          <b-form-group label="Subject:" label-for="subject" class="mb-3">
            <b-form-input
              type="text"
              id="subject"
              name="subject"
              placeholder="Subject"
              required
            ></b-form-input>
          </b-form-group>
          <b-form-group label="Message:" label-for="subject" class="mb-3">
            <b-form-textarea
              id="message"
              name="message"
              placeholder="Message"
              rows="3"
              max-rows="10"
            ></b-form-textarea>
          </b-form-group>
        </form>
      </b-container>
    </div>
  </section>
</template>
<script>
export default {
  name: "Contact",
};
</script>