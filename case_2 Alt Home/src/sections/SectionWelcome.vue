<template>
  <div class="welcome">
    <div class="welcome-content container">
      <h1>Загородные дома в аренду</h1>
      <p class="welcome-city">Санкт-Петербург</p>
      <p class="welcome-text">
        Отдохните от суеты мегаполиса в уютном тёплом доме <br />
        в окружении экологически чистых лесов, рек и озёр
      </p>
      <div class="welcome-button">
        <a href="" class="button"></a>
      </div>
      <ul class="social-media">
        <li class="social-media-item" v-for="(item, key) of socialMediaItems" :key="key">
          <img :src="require('@/assets/icons/' + item.icon)" :alt="item.alt" />
        </li>
      </ul>
      <div class="welcome-img-container" />

      <div class="slider-controls">
        <button class="slider-button slider-button-prev" type="button"></button>
        <button class="slider-button slider-button-next" type="button"></button>
        <p class="slider-page"></p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      socialMediaItems: [
        { icon: 'faceboock.svg', alt: 'Faceboock' },
        { icon: 'insta.svg', alt: 'Instagram' },
        { icon: 'vk.svg', alt: 'VK' }
      ]
    }
  }
}
</script>

<style lang="scss">
.welcome {
  padding-bottom: 100px;
  &-city {
    grid-area: 1 / 2 / 2 / 8;
  }
  h1 {
    grid-area: 2 / 2 / 3 / 8;
    z-index: 1;
  }
  &-text {
    grid-area: 3 / 2 / 4 / 8;
    z-index: 1;
    margin: 10px 0 40px 0;
  }

  &-button {
    grid-area: 4 / 2 / 5 / 4;
    margin-bottom: 90px;
  }

  &-content {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: repeat(5, auto);
    grid-column-gap: 24px;
  }
  &-image-container {
    grid-area: 1 / 6 / -1 / -1;
  }
}

.slider {
  &-controls {
    grid-area: 5 / 6 / 6/ -1;

    display: grid;
    grid-template-columns: auto auto 1fr;
  }
  &-button {
    //@at-ro
    margin: 1;
  }
  &-page {
    margin: 10px 30px 0 0;
    text-align: right;
  }
}

.social-media {
  grid-area: 5 / 2 / 6 / 5;
  padding: 0;
  margin: 10px 0 0 0;
  list-style: none;

  display: flex;
  flex-wrap: wrap;
  align-items: center;

  &-item {
    margin-right: 73px;
    &:last-child {
      margin-right: 0;
    }
  }
}
</style>