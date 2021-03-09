<template>
  <body class="page">
    <TheHeader class="page-header" />
    <Content class="page-content" />
    <TheFooter class="page-footer" />
  </body>
</template>

<script>
import TheFooter from './components/TheFooter'
import TheHeader from './components/TheHeader'
import Content from './components/Content'

export default {
  name: 'App',
  components: {
    TheFooter,
    TheHeader,
    Content
  }
}
</script>

<style lang="scss">
@import './style/normalize.css';
@import './style/base/index';
body {
  margin: 0;
  padding: 0;
  min-width: 1440px;
  font-family: 'Montserrat', 'Arial', sans-serif;
  font-weight: 300;
  font-size: 16px;
  line-height: 32px;
  color: #333333;
}
.page {
  display: grid;
  grid-template-rows: auto 1fr auto;
  grid-template-areas:
    'header'
    'content'
    'footer';
  min-height: 100vh;
}

.visually-hidden {
  position: absolute;
  clip: rect(1px, 1px, 1px, 1px);
  padding: 0;
  border: 0;
  height: 1px;
  width: 1px;
  overflow: hidden;
}
</style>
