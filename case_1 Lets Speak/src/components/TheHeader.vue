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
@import '../style/base/colors';

.page-header {
  grid-area: header;
  display: grid;
  grid-template-columns: 1fr auto 80px;
  background-color: $primaryWhite;
  border-bottom: 1px solid $perano;
  &-input {
    border-style: none;
  }
}
.search {
  margin-top: 10px;
  margin-left: 30px;
  &-field {
    padding: 20px 20px 20px 32px;

    font-family: inherit;
    font-weight: 300;
    font-size: 16px;
    line-height: 19px;
    color: $darkBlue;
    border: none;
    background-image: url('https://assets.htmlacademy.ru/content/skills/6/case-01/img/search.svg');
    background-repeat: no-repeat;
    background-position: left center;
    background-size: 20px 20px;

    &::placeholder {
      color: $perano;
    }
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

    background: $lightBlue;
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

  font-weight: 900;
  font-size: 22px;
  line-height: 40px;
  text-align: center;
  color: $perano;
  border-radius: 50%;
  background-color: $lightBlue;
}

.profile-name {
  font-size: 16px;
  line-height: 40px;
  color: $darkBlue;
  text-decoration: none;
}

.profile-btn {
  position: relative;
  width: 30px;
  border: none;
  background-color: transparent;
  &::before {
    content: '';
    position: absolute;
    width: 0;
    height: 0;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    border: 6px solid $indigo;
    border-left-color: transparent;
    border-right-color: transparent;
    border-bottom-color: transparent;
  }
}

.notifications-btn {
  width: 25px;
  height: 25px;
  margin: 27px;

  background-image: url('https://assets.htmlacademy.ru/content/skills/6/case-01/img/notifications.svg');
  background-repeat: no-repeat;
  background-position: center;
  background-size: 20px 20px;
  background-color: transparent;
  border: none;
  span {
    display: inline-block;
    position: relative;
    right: -5px;
    top: -5px;
    width: 14px;
    height: 14px;
    font-weight: 900;
    font-size: 10px;
    line-height: 14px;
    color: $primaryWhite;
    background-color: $orange;
    border-radius: 50%;
    border: 2px solid $primaryWhite;
  }
}
</style>