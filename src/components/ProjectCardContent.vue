<template>
  <b-card-body :title="title">
    <p class="card-subtitle text-primary">
      {{ stack }}
    </p>
    <p class="card-description">
      <slot>
        This is just a short description made by the brilliant developer Eriq
        John. This is just a filler of this huge space to make it look aesthetic
        for now.
      </slot>
    </p>
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