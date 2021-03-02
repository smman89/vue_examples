<template>
  <footer class="page-footer">
    <p class="copyright h5__regular">© 2020</p>
    <a class="page-footer-logo h5__regular" href="#"> Let’s Speak, языковая школа </a>
    <p class="copyright-details h5__regular"><b>Сайт создан в</b> <a href="htmlacademy.ru">HTML Academy</a></p>
  </footer>
</template>

<style lang="scss" scoped>
@import '../style/base/colors';

.page-footer {
  background-color: $darkBlue;
  grid-area: footer;
  display: grid;
  grid-template-columns: 280px 1fr 280px;
  &-logo {
    margin: 20px 0;
    text-align: center;
  }
}

.copyright {
  margin: 20px 10px 10px 30px;
  color: $text-color--white;
}

.copyright-details {
  text-align: center;
  color: $text-color--white;
  a {
    color: $text-color--white;
  }
}
</style>