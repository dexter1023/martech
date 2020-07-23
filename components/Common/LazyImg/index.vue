<template>
  <figure>
    <img :data-src="src" :alt="alt" />
  </figure>
</template>
<script>
export default {
  props: {
    src: {
      required: true,
      type: String,
    },
    alt: {
      default: '',
      type: String,
    },
  },
}
</script>
