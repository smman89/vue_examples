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
@import '../../style/base/colors';

.offers {
  grid-area: offers;
}
.offer {
  &-list {
    padding: 0;
    margin: 0;
    list-style: none;

    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 20px;
  }

  &-item {
    display: grid; /* для выравнивания ссылки */
    grid-template-rows:
      auto
      1fr
      auto;
    padding: 20px 30px;

    background-color: #ffffff;
    box-shadow: 0 1px 4px rgba(60, 66, 95, 0.2);
    border-radius: 4px;

    &-text {
      margin: 5px 0 5px 0;
      font-weight: 300;
      font-size: 14px;
      line-height: 20px;
      color: #3c425f;
    }

    &-time {
      margin: 0 0 8px 0;
      font-weight: 900;
      font-size: 14px;
      line-height: 20px;
      color: #0bc4cf;
    }

    a {
      font-weight: 500;
      font-size: 16px;
      line-height: 20px;
      color: #576bcc;
      text-decoration: none;
    }
  }
  &-footer {
    text-align: right;
  }
}
</style>