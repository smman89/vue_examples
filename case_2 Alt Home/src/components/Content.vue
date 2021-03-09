<template>
  <main class="page-content">
    <SectionWelcome />
    <ArticleLake />
  </main>
</template>

<script>
import SectionWelcome from '../sections/SectionWelcome'
import ArticleLake from '../sections/ArticleLake'

export default {
  components: {
    SectionWelcome,
    ArticleLake
  }
}
</script>


<style lang="scss" scoped>
.page-content {
  grid-area: content;
}
</style>