<template>
  <header class="page-header">
    <div class="search">
      <form method="GET" action="#">
        <input
          class="search-field"
          type="text"
          name="search"
          id="search"
          placeholder="Поиск..."
        />
      </form>
    </div>
    <div class="profile item-with-picture" data-text="О">
      <a class="profile-name" href="#">Опознанный Енот</a>
      <button class="profile-btn" type="button">
        <span class="visually-hidden">Открыть/Закрыть меню</span>
      </button>
    </div>
    <div class="notifications">
      <button class="notifications-btn" type="button"><span>1</span></button>
    </div>
  </header>
</template>

<style lang="scss" scoped>
.page-header {
  grid-area: header;
  display: grid;
  grid-template-columns: 1fr auto auto auto;
  &-input {
    border-style: none;
  }
}
.search {
  grid-column: 1/2;
  &-field {
    height: 100px;
  }
}
.user {
  grid-column: 2/3;
  &-logo {
    display: inline-block;
    position: absolute;
    width: 40px;
    height: 40px;
    left: 1115px;
    top: 20px;

    background: #f1f3fe;
    border-radius: 20px;
  }
}
</style>