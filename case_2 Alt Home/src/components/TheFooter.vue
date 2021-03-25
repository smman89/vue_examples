<template>
  <footer class="page-footer">
    <div class="page-footer-wrapper container">
      <a class="page-footer-logo" href="#">
        <img
          src="https://assets.htmlacademy.ru/content/skills/6/case-02/img/logo-footer.svg"
          width="97"
          height="30"
          alt="Логотип компании Alt Home"
        />
      </a>
      <ul class="page-footer-nav">
        <li class="page-footer-nav-item" v-for="(link, key) of links" :key="key">
          <a class="page-footer-nav-link page-link" href="#">{{ link.title }}</a>
        </li>
      </ul>
      <p class="copyright"></p>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      links: [{ title: 'Место' }, { title: 'Каталог' }, { title: 'Оставить заявку' }]
    }
  }
}
</script>


<style lang="scss" >
.page {
  &-link {
    text-decoration: none;
    font-weight: normal;
    font-size: 16px;
    line-height: 20px;
    color: #06a9b3;
  }
  &-footer {
    grid-area: footer;
    background-color: #f2f8fb;
    &-wrapper {
      display: grid;
      grid-template-columns: auto 1fr auto;
    }
    &-logo {
      margin: 30px 0;
    }

    &-nav {
      padding: 0 0 0 135px;
      margin: 0;
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      align-items: center;

      &-item {
        padding-right: 65px;
      }
    }
  }
}

.copyright {
  margin-top: 30px;
}
</style>