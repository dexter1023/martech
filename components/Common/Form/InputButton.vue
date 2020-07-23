<template>
  <div class="wrapper font-normal">
    <input
      type="text"
      :placeholder="placeholder"
      :aria-placeholder="placeholder"
    />
    <button>{{ text }}</button>
  </div>
</template>
<script>
export default {
  props: {
    placeholder: {
      type: String,
      default: '',
    },
    text: {
      type: String,
      default: '',
    },
  },
}
</script>
<style lang="scss" scoped>
.wrapper {
  display: inline-block;
}
input {
  max-width: 50%;
  color: $white;
  background-color: rgba(0, 0, 0, 0.1);
  border-radius: 5px 0 0 5px;
  border: 0;
  font-size: $font-normal;
  padding: 12px 18px;
  outline: none;
  &::placeholder {
    font-size: $font-normal;
  }
}
button {
  position: relative;
  left: -4px;
  max-width: 50%;
  background-color: $teal;
  color: $white;
  padding: 11px 18px;
  font-size: $font-normal;
  border: 0;
  border-radius: 0px 5px 5px 0;
}
</style>
