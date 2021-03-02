<template>
  <section class="offers">
    <ul class="offer-list">
      <li class="offer-item box" v-for="(offer, key) of offers" :key="key">
        <h3>
          {{ offer.title }}
        </h3>
        <div class="offer-content">
          <p class="offer-item-text">
            {{ offer.text }}
          </p>
          <p class="offer-item-time" v-if="offer.time">
            {{ offer.time }}
          </p>
          <div class="offer-footer">
            <a href="#">Записаться ➞</a>
          </div>
        </div>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  data() {
    return {
      offers: [
        {
          title: 'Английский завтрак',
          content: 'Разговорный клуб',
          time: '10:00 - 11:00 (ПН-ПТ)'
        },
        {
          title: 'Лето в Лондоне',
          content: 'Месяц экскурсий и практики',
          time: '10 июня - 3 июля'
        },
        {
          title: 'Надоел английский?',
          content: 'С нами можно выучить и другие языки'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.offers {
  grid-area: offers;
}
.offer {
  &-list {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 20px;
    list-style: none;
  }
  &-footer a {
    text-decoration: none;
  }
}
</style>