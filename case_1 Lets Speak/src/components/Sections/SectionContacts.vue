<template>
  <section class="contacts box">
    <h2>Контакты</h2>
    <ul class="contact-list">
      <li class="contact-item" v-for="(contact, key) of contacts" :key="key">
        <a class="contact-link item-with-picture" data-text="H" href="#">
          <p class="contatct-name">{{ contact.name }}</p>
          <p class="contatct-lang">{{ contact.lang }}</p>
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

  h2 {
    text-decoration: underline;
  }
}

.contact {
  &-list {
    list-style: none;
  }
}
</style>