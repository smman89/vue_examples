<template>
  <nav class="page-menu">
    <Logo class="logo" />
    <ul class="page-menu-list">
      <li
        v-for="(menu, key) of menuList"
        :key="key"
        :class="'page-menu-item ' + (menu.isActive ? 'page-menu-item-active' : '')"
      >
        <img :src="require('@/assets/icons/' + menu.icon)" :alt="menu.title" />
        <a class="page-menu-item-link" href="#">{{ menu.title }}</a>
      </li>
    </ul>
    <ul class="page-menu-tools">
      <li class="page-menu-item">
        <img :src="require('@/assets/icons/tools.svg')" alt="Настройки" />
        <a class="page-menu-item-link" href="#">Настройки</a>
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
        { title: 'Кабинет ученика', icon: 'studentsOffice.svg', isActive: true },
        { title: 'Учебный класс', icon: 'hat.svg', isActive: false },
        { title: 'Методика', icon: 'boock.svg', isActive: false },
        { title: 'Домашняя работа', icon: 'completedList.svg', isActive: false }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../style/base/colors';

.logo {
  margin: 24px 30px 15px;
}
.page-menu {
  grid-area: navigation;
  display: grid;
  grid-template-rows:
    80px
    1fr
    auto;

  border-right: 1px solid $perano;

  &-tools {
    padding: 0;
    margin: 0 0 10px 0;
    list-style: none;
    &-item {
      display: grid;
      grid-template-columns: auto 1fr;
    }
    &-link {
      position: relative;
      display: block;
      padding: 20px 25px 20px 63px;

      font-size: 16px;
      line-height: 20px;
      color: $darkBlue;
      text-decoration: none;
    }
  }

  &-list {
    padding: 0;
    margin: 0;
    list-style: none;
    justify-items: start;
    grid-template-columns: 1fr;
  }

  &-item {
    display: grid;
    grid-template-columns: auto 1fr;
    img {
      background-repeat: no-repeat;
      background-position: center;
      margin: auto 20px;
    }
    &-link {
      position: relative;
      display: block;
      padding: 20px 0;

      font-size: 16px;
      line-height: 20px;
      color: $darkBlue;
      text-decoration: none;
    }
    &-active {
      background-color: $lightBlue;
      .page-menu-link {
        font-weight: 500;
        color: $indigo;
      }
    }
  }
}
</style>