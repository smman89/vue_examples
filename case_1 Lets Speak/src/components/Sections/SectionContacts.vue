<template>
  <section class="contacts box">
    <h3>Контакты</h3>
    <ul class="contact-list">
      <li class="contact-item" v-for="(contact, key) of contacts" :key="key">
        <a class="contact-link item-with-picture" data-text="H" href="#">
          <p class="contact-name">{{ contact.name }}</p>
          <p class="contact-lang">{{ contact.lang }}</p>
        </a>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  data() {
    return {
      contacts: [
        { name: 'Неопознанный Енот', lang: 'English A1' },
        { name: 'Неопознанный Енот 2', lang: 'Español 2' },
        { name: 'Неопознанный Енот 3', lang: '日本語' },
        { name: 'Неопознанный Енот 4', lang: 'English B2' },
        { name: 'Неопознанный Енот 5', lang: 'Le Français' },
        { name: 'Неопознанный Енот 6', lang: 'Español 1' },
        { name: 'Неопознанный Енот 7', lang: 'Italiano' }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import '../../style/base/index';

.contacts {
  grid-area: contacts;

  padding: 20px 0 20px 30px;

  background-color: #ffffff;
  box-shadow: 0 1px 4px rgba(60, 66, 95, 0.2);
  border-radius: 4px;
}

.contact {
  &-list {
    padding: 5px 0 0 0;
    margin: 0;
    list-style: none;

    border-top: 1px solid #e4e8fc;
  }
  &-item {
    padding: 16px 10px 0 0;
  }

  &-link {
    display: grid;
    grid-template-columns: 40px auto;
    grid-template-rows:
      auto
      auto;
    grid-column-gap: 12px;

    text-decoration: none;
    font-weight: 300;
    font-size: 14px;
    line-height: 20px;
    color: #3c425f;
    &::before {
      grid-row: 1 / 3;
    }
  }
  &-name {
    grid-column: 2 / 3;
    grid-row: 1 / 2;
    margin: 0;
  }
  &-lang {
    grid-column: 2 / 3;
    grid-row: 2 / 3;
    margin: 0;
  }
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
</style>