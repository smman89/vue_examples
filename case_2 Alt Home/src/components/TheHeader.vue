<template>
  <header class="page-header">
    <nav class="page-nav container">
      <ul class="site-nav">
        <li class="site-nav-item" v-for="(item, key) of navigationLinks" :key="key">
          <a class="site-nav-link page-link" href="#">{{ item.title }}</a>
        </li>
      </ul>
      <div class="logo-container">
        <a href="#" class="logo">
          <img
            src="https://assets.htmlacademy.ru/content/skills/6/case-02/img/logo.svg"
            width="97"
            height="30"
            alt="Логотип компании Alt Home"
          />
        </a>
      </div>
      <div class="search-container">
        <a href="" class="search"></a>
      </div>
      <div class="user-nav">
        <a class="page-link" href="#">Вход</a> или <a class="page-link" href="#">регистрация</a>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  data() {
    return {
      navigationLinks: [{ title: 'Место' }, { title: 'Каталог' }, { title: 'Оставить заявку' }]
    }
  }
}
</script>


<style lang="scss" scoped>
.page {
  &-header {
    grid-area: header;
    background-color: #f2f8fb;
  }
  &-nav {
    display: grid;
    grid-template-columns: auto 1fr auto auto;
    grid-column-gap: 65px;
  }
}
.logo-container {
  padding: 20px 110px 20px 0;
  text-align: center;
}
.search-container {
  padding: 25px 0 23px;
}
.user-nav {
  padding: 25px 0 23px;
}

.site-nav {
  padding: 0;
  margin: 0;
  list-style: none;
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  &-item {
    padding-right: 65px;
    &:last-child {
      padding-right: 0;
    }
  }
}
</style>