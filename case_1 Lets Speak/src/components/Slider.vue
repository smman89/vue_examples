<template>
  <div class="slider">
    <img
      src="https://assets.htmlacademy.ru/content/skills/6/case-01/img/image-01.jpg"
      alt="Бигбен на фоне голубого облачного неба"
      width="820"
      height="300"
    />

    <p class="slider-headline">«Бифитер», «Кокни», «Даблдекер»...</p>
    <p class="slider-text">Пройдите тест и узнайте насколько хорошо вы знакомы с жизнью в Лондоне</p>
    <a href="#">Пройти тест ➞</a>
    <button class="slider-btn slider-btn-prev" type="button"></button>
    <button class="slider-btn slider-btn-next" type="button"></button>
  </div>
</template>

<style scoped lang="scss">
.slider {
  position: relative;
  grid-area: slider;
  width: 820px;
  height: 300px;
  padding: 32px 60px;
  overflow: hidden;
  box-sizing: border-box;

  a {
    position: relative;
    padding: 10px 20px;
  }

  &-img {
    position: absolute;
    left: 0;
    top: 0;
  }
  &-text {
    position: relative;
    margin: 0 0 30px 0;
    max-width: 470px;
  }

  &-btn {
    position: absolute;
    width: 64px;
    height: 64px;
    left: -32px;
    top: 0;
    bottom: 0;
    margin: auto;
    border-radius: 50%;
    border: none;
  }
  &-headline {
    position: relative;
    margin-bottom: 10px;
  }
  &-btn-next {
    left: auto;
    right: -32px;
    top: 0;
    bottom: 0;
    margin: auto;
  }
}
</style>