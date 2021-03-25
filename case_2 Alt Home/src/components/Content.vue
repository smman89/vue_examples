<template>
  <main class="page-content">
    <SectionWelcome />
    <ArticleLake />
    <SectionCatalog />
    <SectionOrder />
  </main>
</template>

<script>
import SectionWelcome from '../sections/SectionWelcome'
import ArticleLake from '../sections/ArticleLake'
import SectionCatalog from '../sections/SectionCatalog'
import SectionOrder from '../sections/SectionOrder'

export default {
  components: {
    SectionWelcome,
    ArticleLake,
    SectionCatalog,
    SectionOrder
  }
}
</script>


<style lang="scss" scoped>
.page-content {
  grid-area: content;
}
</style>