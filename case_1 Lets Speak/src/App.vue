<template>
  <body class="hg container">
    <Menu />
    <TheHeader />
    <Content />
    <Contacts />
    <TheFooter />
  </body>
</template>

<script>
import TheFooter from "./components/TheFooter";
import TheHeader from "./components/TheHeader";
import Contacts from "./components/Contacts";
import Content from "./components/Content";
import Menu from "./components/Menu";

export default {
  name: "App",
  components: {
    TheFooter,
    TheHeader,
    Contacts,
    Content,
    Menu,
  },
};
</script>

<style >
@import "./style/normalize.css";
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.hg {
  display: grid;
  grid-template-columns: 280px 1fr 280px;
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
