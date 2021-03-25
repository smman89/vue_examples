<template>
  <section class="section catalog">
    <div class="container">
      <header class="section-centered-heading">
        <h2>Каталог</h2>
        <h3>Дома для аренды</h3>
      </header>
      <div class="catalog-content">
        <div
          :class="'card-item ' + (house.image === '5.jpg' ? 'card-horizontal' : '')"
          v-for="(house, key) of houses"
          :key="key"
        >
          <img class="card-pic" :src="require('@/assets/houses/' + house.image)" :alt="house.title" />
          <div class="card-content">
            <h3>{{ house.title }}</h3>
            <p>Площадь - {{ house.square }}м<sup>2</sup></p>
            <dl>
              <dt>комнат</dt>
              <dd>{{ house.rooms }}</dd>
              <dt>спальни</dt>
              <dd>{{ house.badrooms }}</dd>
              <dt>этажа</dt>
              <dd>{{ house.stages }}</dd>
            </dl>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      houses: [
        { title: 'Современная классика', image: '1.jpg', square: 186, rooms: 5, badrooms: 3, stages: 2 },
        { title: 'Дом на берегу озера', image: '2.jpg', square: 186, rooms: 5, badrooms: 3, stages: 2 },
        { title: 'Особняк в лесу', image: '3.jpg', square: 186, rooms: 5, badrooms: 3, stages: 2 },
        { title: 'Домик на дереве', image: '4.jpg', square: 186, rooms: 5, badrooms: 3, stages: 2 },
        { title: 'Лесной дом у пруда', image: '5.jpg', square: 186, rooms: 5, badrooms: 3, stages: 2 }
      ]
    }
  }
}
</script>

<style lang="scss" >
@import '../style/base/colors';

.section-centered-heading {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 100px;
  padding-bottom: 13px;
}
.catalog {
  padding: 0 0 140px 0;
  background-color: #f2f8fb;

  &-content {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    gap: 24px;
  }
}

.card {
  &-pic {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  &-content {
    padding: 0 24px 23px;

    h3 {
      margin: 0 0 5px 0;
      font-weight: normal;
      font-size: 22px;
      line-height: 34px;
      color: #333333;
    }

    p {
      margin: 0 0 17px 0;

      font-weight: 400;
      font-size: 16px;
      line-height: 19px;
      color: #aaaaaa;
    }

    dt {
      margin: 0;
      font-weight: 300;
      font-size: 16px;
      line-height: 20px;
    }

    dd {
      margin: 0;
      grid-row: 1 / 2;
      font-weight: 300;
      font-size: 32px;
      line-height: 36px;
    }

    dl {
      margin: 0;
      padding: 15px 0 0 0;
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      grid-column-gap: 50px;
      border-top: 2px solid #eaf2f6;
    }
  }
  &-item {
    grid-column: span 3;
    border: 1px solid $gray;

    display: grid;
    grid-template-columns: 3fr;
    grid-template-rows:
      220px
      auto;
    grid-gap: 17px 24px;
    background-color: #ffffff;
  }

  &-horizontal {
    grid-column: 3 / -3;
    grid-template-columns: 3fr 5fr;
    grid-template-rows: auto;

    .card-content {
      padding: 20px 24px 24px 0;
    }
  }
}
</style>