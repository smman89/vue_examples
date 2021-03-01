<template>
  <body class="page container">
    <Menu />
    <TheHeader />
    <Content />
    <TheFooter />
  </body>
</template>

<script>
import TheFooter from './components/TheFooter'
import TheHeader from './components/TheHeader'
import Content from './components/Content'
import Menu from './components/Menu'

export default {
  name: 'App',
  components: {
    TheFooter,
    TheHeader,
    Content,
    Menu
  }
}
</script>

<style >
@import './style/normalize.css';
#app {
  padding: 0;
  margin: 0;
  font-family: 'Roboto', 'Arial', sans-serif;
  font-weight: 300;
  font-size: 14px;
  line-height: 20px;
  color: #3c425f;
}

.page {
  display: grid;
  grid-template-areas:
    'navigation header'
    'navigation main'
    'footer footer';
  grid-template-columns: 280px 1fr;
  grid-template-rows:
    80px
    1fr
    60px;
  grid-gap: 30px;
  min-height: 100vh;
}
.container {
  width: 1440px;
  margin: 0 auto;
}
</style>
