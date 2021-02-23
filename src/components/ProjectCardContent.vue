<template>
  <b-card-body :title="title" class="d-flex flex-column h-100">
    <p class="card-subtitle text-primary">
      {{ stack }}
    </p>
    <p class="card-description">
      This is just a short description made by the brilliant developer Eriq
      John. This is just a filler of this huge space to make it look aesthetic
      for now.
    </p>
    <div class="mt-auto text-center">
      <b-button variant="outline-primary" @click="$emit('open')">
        Learn More
      </b-button>
    </div>
  </b-card-body>
</template>
<script>
export default {
  props: {
    title: {
      required: true,
      type: String,
    },
    stack: {
      required: true,
      type: String,
    },
  },
};
</script>