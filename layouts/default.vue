<template>
  <div>
    <Header />
    <div>
      <div class="content__main">
        <Nuxt />
      </div>
    </div>
    <Footer />
  </div>
</template>
<script>
import Header from '@/components/Header'
export default {
  components: {
    Header,
  },
}
</script>
<style lang="scss" scoped>
.content__layer {
  background-color: rgba(0, 0, 0, 0.1);
  width: 100%;
  height: 100%;
}
.content__layer * {
  opacity: 1;
}
.content__main {
  width: 100%;
}
</style>
