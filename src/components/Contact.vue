<template>
  <section id="contact">
    <div class="offset">
      <b-container>
        <h1 class="text-center section-title text-white">Contact</h1>

        <form action="" id="contact-form" class="glass-background">
          <div class="mb-3">
            <label for="first_name" class="form-label"> First Name </label>
            <input
              type="text"
              class="form-control"
              id="first_name"
              placeholder="First Name"
            />
          </div>
          <div class="mb-3">
            <label for="last_name" class="form-label"> Last Name </label>
            <input
              type="text"
              class="form-control"
              id="last_name"
              placeholder="Last Name"
            />
          </div>
          <div class="mb-3">
            <label for="email" class="form-label"> Email Address </label>
            <input
              type="email"
              class="form-control"
              id="email"
              placeholder="Email Address"
            />
          </div>
          <div class="mb-3">
            <label for="subject" class="form-label"> Subject </label>
            <input
              type="text"
              class="form-control"
              id="subject"
              placeholder="Subject"
            />
          </div>
          <div class="mb-3">
            <label for="message" class="form-label"> Message </label>
            <textarea class="form-control" id="message" rows="5"></textarea>
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