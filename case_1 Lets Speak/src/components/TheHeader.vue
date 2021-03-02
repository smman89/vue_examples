<template>
  <header class="page-header">
    <div class="search">
      <form method="GET" action="#">
        <input class="search-field" type="text" name="search" id="search" placeholder="Поиск..." />
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
  grid-template-columns: 1fr auto 80px;
  &-input {
    border-style: none;
  }
}
.search {
  margin-top: 10px;
  margin-left: 30px;
  &-field {
    padding: 20px 20px 20px 32px;
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

.profile {
  display: grid;
  grid-template-columns: repeat(3, auto);
  grid-gap: 10px;
  max-width: 400px;
  margin-top: 20px;
  margin-bottom: 20px;
  margin-right: 20px;
}

.item-with-picture::before {
  content: attr(data-text);
  width: 40px;
  height: 40px;
}

.profile-name {
  /* Временно для сетки */
  min-width: 130px;
}

.profile-btn {
  width: 30px;
  border: none;
  background-color: transparent;
}

.notifications-btn {
  width: 25px;
  height: 25px;
  margin: 27px;
}
</style>