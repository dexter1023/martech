<template>
  <div class="item">
    <img :src="require(`../../../assets/img/shapes/${logo}`)" alt="Icon" />
    <span class="tk-museo-sans-rounded">{{ text }}</span>
  </div>
</template>
<script>
export default {
  props: {
    text: {
      type: String,
      required: true,
    },
    logo: {
      type: String,
      required: true,
    },
  },
}
</script>
<style lang="scss" scoped>
.item {
  display: flex;
  align-content: center;
  margin-bottom: 20px;
  img {
    margin-right: 23px;
    width: 26px;
    height: 26px;
    filter: invert(26%) sepia(72%) saturate(4603%) hue-rotate(320deg)
      brightness(92%) contrast(96%);
  }
  span {
    font-size: 18px;
    color: $white;
  }
}
</style>
