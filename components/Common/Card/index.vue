<template>
  <div class="card">
    <div class="card__title tk-museo-sans-rounded font-bold">
      {{ title }}
    </div>
    <div class="card__body">
      <slot />
    </div>
  </div>
</template>
<script>
export default {
  props: {
    title: {
      type: String,
      default: '',
    },
  },
}
</script>
<style lang="scss" scoped>
.card {
  padding: 48px 123px;
  background: $white;
  border: 1px solid $light-gray;
  border-radius: 19px;
}
.card__title {
  font-size: $font-header;
  padding-bottom: 34px;
}
</style>
