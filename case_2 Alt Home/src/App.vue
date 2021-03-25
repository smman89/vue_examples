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
@import './style/components/index';

.section {
  h2 {
    position: relative;
    margin: 0;
    padding: 0 0 0 115px;
    font-weight: normal;
    font-size: 16px;
    line-height: 20px;
    color: #06a9a3;
  }
  h2::before {
    counter-increment: section-counter; /* Инкрементирует счетчик*/
    content: '0' counter(section-counter); /* Отображает текущее значение счетчика */
    position: absolute;
    left: 0;
    top: 0;
    font-weight: 300;
    font-size: 16px;
    line-height: 20px;
    color: #06a9b3;
  }

  h2::after {
    content: '';
    position: absolute;
    width: 81px;
    height: 1px;
    left: 25px;
    top: 9px;
    border-top: 1px solid #06a9b3;
  }
  h3 {
    margin: 60px 0 25px 0;
    font-size: 32px;
    line-height: 48px;
  }
}

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
