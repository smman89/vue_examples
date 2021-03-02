<template>
  <nav class="page-menu">
    <Logo />
    <ul class="page-menu-list">
      <li v-for="(menu, key) of menuList" :key="key" class="page-menu-item">
        <img :src="require('@/assets/icons/' + menu.icon)" :alt="menu.title" /><a
          class="page-menu-item-link"
          href="#"
          >{{ menu.title }}</a
        >
      </li>
    </ul>
    <ul class="page-menu-tools">
      <li class="page-menu-tools-item">
        <img :src="require('@/assets/icons/tools.svg')" alt="tools" />
        <a class="menu-item-title" href="#">Настройки</a>
      </li>
    </ul>
  </nav>
</template>

<script>
import Logo from './Logo'
export default {
  components: { Logo },
  data() {
    return {
      menuList: [
        { title: 'Кабинет ученика', icon: 'studentsOffice.svg' },
        { title: 'Учебный класс', icon: 'hat.svg' },
        { title: 'Методика', icon: 'boock.svg' },
        { title: 'Домашняя работа', icon: 'completedList.svg' }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.page-menu {
  grid-area: navigation;
  display: grid;
  grid-template-rows:
    80px
    1fr
    auto;
  &-list {
    padding: 0;
    margin: 0;
    list-style: none;
    justify-items: start;
    grid-template-columns: 1fr;
  }
  &-tools {
    padding: 0;
    margin: 0;
    list-style: none;
  }

  &-item {
    padding: 20px;
    &-link {
      padding-left: 20px;
    }
  }
}
</style>