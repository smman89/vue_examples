<template>
  <div class="slider">
    <img
      src="https://assets.htmlacademy.ru/content/skills/6/case-01/img/image-01.jpg"
      alt="Бигбен на фоне голубого облачного неба"
      width="820"
      height="300"
      class="slider-img"
    />

    <p class="slider-headline p__heading">«Бифитер», «Кокни», «Даблдекер»...</p>
    <p class="slider-text">Пройдите тест и узнайте насколько хорошо вы знакомы с жизнью в Лондоне</p>
    <a class="link__primary" href="#">Пройти тест ➞</a>
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
    text-decoration: none;
    background-color: #ff8f0b;
    border-radius: 4px;
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
    color: #ffffff;
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

    background-color: #ffffff;
    background-image: url('https://assets.htmlacademy.ru/content/skills/6/case-01/img/arrow.svg');
    background-repeat: no-repeat;
    background-position: left 35px center;
    background-size: 18px 18px;

    &-next {
      transform: rotate(180deg);
    }
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