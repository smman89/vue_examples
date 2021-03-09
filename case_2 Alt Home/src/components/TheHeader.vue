<template>
  <header class="page-header">
    <nav class="page-nav container">
      <ul class="site-nav">
        <li class="site-nav-item" v-for="(item, key) of navigationLinks" :key="key">{{ item.title }}</li>
      </ul>
      <div class="logo-container">
        <a href="#" class="logo"></a>
      </div>
      <div class="search-container">
        <a href="" class="search"></a>
      </div>
      <div class="user-nav">
        <a href="" class="page-link"></a>
        <a href="" class="page-link"></a>
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