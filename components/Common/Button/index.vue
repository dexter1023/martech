<template>
  <button
    class="button"
    :class="{ 'full-width': fullWidth }"
    @click="$emit('click', $event)"
  >
    <slot />
  </button>
</template>
<script>
export default {
  props: {
    fullWidth: {
      type: Boolean,
      default: false,
    },
  },
}
</script>
<style lang="scss" scoped>
@keyframes button-hover {
  0% {
    width: 2px;
  }
  50% {
    left: 25%;
    width: 50%;
  }
  100% {
    width: 2px;
    right: -2px;
    left: 100%;
  }
}
.button {
  position: relative;
  z-index: 10;
  background: $pink;
  border-radius: 5px;
  border: 0;
  color: $white;
  padding: 12px 24px;
  font-size: $font-medium;
  &:hover::after {
    content: '';
    position: absolute;
    border: 3px solid $teal;
    border-right: 0;
    border-left: 0;
    left: -2px;
    width: 2px;
    top: -2px;
    bottom: -2px;
    border-radius: 5px;
    animation: button-hover 0.7s infinite;
  }
}
.full-width {
  width: 100%;
}
</style>
