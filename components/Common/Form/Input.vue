<template>
  <div class="input__wrapper">
    <input :type="type" @input="$emit('input', $event)" :id="id" />
    <label :for="id">{{ label }}</label>
  </div>
</template>
<script>
export default {
  props: {
    type: {
      default: 'text',
      type: String,
    },
    label: {
      default: '',
      type: String,
    },
    value: {
      default: '',
      type: String || Number,
    },
  },
  computed: {
    id() {
      return `id-${this.label}-${this.inputType}`
    },
  },
}
</script>
<style lang="scss" scoped>
.input__wrapper {
  position: relative;
  width: 100%;
  margin-top: 36px;
  label {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    font-size: $font-normal;
    color: $gray;
    transition: 0.2s top;
  }
  input {
    width: 100%;
    border: 0;
    border-bottom: 3px solid $gray;
    padding: 8px;
    &:focus {
      border-bottom: 3px solid $teal;
      outline: none;
    }
    &:focus + label {
      font-size: $font-label;
      color: $teal;
      top: -20px;
    }
  }
}
</style>
