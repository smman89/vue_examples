<template>
  <article class="section place container">
    <header>
      <h2>Парк отдыха на берегу</h2>
      <h3></h3>
    </header>
    <div class="place-content">
      <p>
        Отдохните в уютных деревянных домах с камином, сауной и джакузи, расположенных на берегу озера. Для любителей
        полного уединения есть домики и в глубине парка, в окружении вековых деревьев.
      </p>
      <img
        src="https://assets.htmlacademy.ru/content/skills/6/case-02/img/article-pic1.jpg"
        width="444"
        height="280"
        alt="Домик в лесу"
      />
      <p class="article-aside-right">
        За счёт особой конструкции в наших домах очень тепло зимой и прохладно летом. Мы открыты для вас в любое время
        года!
      </p>

      <p>
        На территории парка есть баскетбольная площадка, собственный пляж с сеткой для волейбола, прокат горных
        велосипедов и лодок. А зимой у нас можно взять в прокат лыжи или снегоходы и кататься по специально
        оборудованным трассам. Для каждого посетителя составляем индивидуальную программу развлечений и помогаем её
        осуществить.
      </p>
      <img
        src="https://assets.htmlacademy.ru/content/skills/6/case-02/img/article-pic2.jpg"
        width="1146"
        height="280"
        alt="Мужчины играют в пляжный волейбол"
        class="big-pic"
      />
      <p>
        Около каждого коттеджа есть детская площадка с качелями и горками, а на территории парка работает детская
        комната. Вы сможете позволить себе любой отдых зная, что ваш ребёнок находится под присмотром опытных
        специалистов.
      </p>
      <blockquote>
        Мы предлагаем не только уютные дома, большой выбор развлечений и активностей для вас и вашей семьи, но и
        масштабные праздники, спортивные турниры и возможность встретить новых друзей.
      </blockquote>
      <p>
        Несмотря на отдалённость от населённых пунктов, вы не будете чувствовать себя оторванными от цивилизации. Все
        наши дома оборудованы высокоскоростными точками доступа Wi-Fi и домашними кинотеатрами с подпиской Netflix.
      </p>
      <p class="article-aside-left">
        Вы можете подписаться на рассылку и узнавать обо всех акциях, скидках, и выгодных предложениях.
      </p>
      <p>
        Приезжайте к нам на месяц, всё лето или зиму — на длительную аренду действуют хорошие скидки! Забронируйте дом
        прямо сейчас, для этого достаточно заказать звонок, а отменить бронь вы сможете в любое время совершенно
        бесплатно.
      </p>
      <div class="place-button-container">
        <a class="button" href="#">Бесплатно забронировать</a>
      </div>
    </div>
  </article>
</template>

<style lang="scss">
.place {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  column-gap: 24px;
  margin-top: 100px;
  margin-bottom: 95px;
  &-button-container {
    grid-column: 5/8;
    margin-top: 10px;
  }
  header {
    grid-column: 5/9;
  }
  &-content {
    grid-column: 1 / -1;

    display: grid;
    grid-template-columns: repeat(12, 1fr);
    column-gap: 24px;
  }
  &-content {
    > * {
      grid-column: 5 / 9;
    }
    p {
      margin-top: 0;
      margin-bottom: 25px;
    }
    img {
      margin: 0 0 25px 0;
    }

    blockquote {
      grid-column: 4 / 10;
      margin: 0 0 35px 0;
      padding-left: 30px;

      font-weight: normal;
      font-size: 22px;
      line-height: 40px;
      border-left: 1px solid #06a9b3;
    }
  }
}
.big-pic {
  grid-column: 2 / -2;
}
.article-aside {
  &-left {
    grid-column: 2/4;
    margin-top: 20px;

    font-weight: 300;
    font-size: 14px;
    line-height: 24px;
  }
  &-right {
    grid-column: -4/-2;
  }
}
</style>