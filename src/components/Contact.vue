<template>
  <section id="contact">
    <div class="offset">
      <b-container class="contact-container">
        <h1 class="text-center section-title text-white" data-aos="fade-down">
          Contact
        </h1>

        <b-alert
          show
          variant="warning"
          class="contact-alert mx-auto"
          data-aos="zoom-in"
          data-aos-duration="1500"
        >
          This form is for demonstration purposes only. You can reach me at
          <code>mendozaeriqjohn48@gmail.com</code>
        </b-alert>

        <form
          action=""
          id="contact-form"
          class=""
          data-aos="zoom-in"
          data-aos-duration="1500"
          data-aos-delay="500"
        >
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
          <div class="contact-submit-container">
            <b-button
              block
              pill
              variant="success"
              class="contact-submit-button"
              type="submit"
            >
              Submit
            </b-button>
          </div>
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