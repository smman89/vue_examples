<template>
  <nav class="menu">
    <ul class="menu-list">
      <li v-for="(menu, key) of menuList" :key="key" class="menu-item">
        <img
          :src="require('@/assets/icons/' + menu.icon)"
          :alt="menu.title"
        /><a class="menu-item-title" href="#">{{ menu.title }}</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      menuList: [
        { title: "Кабинет ученика", icon: "studentsOffice.svg" },
        { title: "Учебный класс", icon: "hat.svg" },
        { title: "Методика", icon: "boock.svg" },
        { title: "Домашняя работа", icon: "completedList.svg" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
ul {
  list-style: none;
}
.menu {
  grid-column: 1 / 2;
  grid-row: 2 / -2;
  &-list {
    display: grid;
    justify-items: start;
    grid-template-columns: 1fr;
  }
  &-item {
    padding: 20px;
    &-title {
      padding-left: 20px;
    }
  }
}
</style>