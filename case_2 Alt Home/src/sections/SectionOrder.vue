<template>
  <section class="section feedback container">
    <header>
      <h2>Оставить заявку</h2>
      <h3>Мы свяжемся с вами</h3>
    </header>
    <form class="feedback-form" method="get" action="#">
      <div class="titles">
        <label for="titles">Обращение</label>
        <select class="field" name="titles" id="titles"></select>
      </div>
      <div class="name">
        <label for="name">Имя</label>
        <input class="field" type="text" name="name" id="name" />
      </div>
      <div class="surname">
        <label for="surname">Фамилия</label>
        <input class="field" type="text" name="surname" id="surname" />
      </div>
      <div class="email">
        <label for="email">E-mail</label>
        <input class="field" type="email" name="email" id="email" />
      </div>
      <div class="phone">
        <label for="tel">Телефон</label>
        <input class="field" type="tel" name="tel" id="tel" />
      </div>
      <div class="policy checkbox">
        <input class="visually-hidden" type="checkbox" name="agreement" id="agreement" />
        <label for="agreement" class="text-label"></label>
      </div>
      <div class="subscribe checkbox">
        <input class="visually-hidden" type="checkbox" name="subscribe" id="subscribe" checked />
        <label for="subscribe" class="text-label">Согласие на обработку персональных данных</label>
      </div>
      <div class="subscribe checkbox">
        <input class="visually-hidden" type="checkbox" name="subscribe" id="subscribe" checked />
        <label for="subscribe" class="text-label">Подписка на рассылку</label>
      </div>
      <div class="submit">
        <button class="button" type="submit">Отправить</button>
      </div>
    </form>
    <img
      class="feedback-img"
      src="https://assets.htmlacademy.ru/content/skills/6/case-02/img/form-pic.jpg"
      width="708"
      height="737"
      alt="Лодка на озере"
    />
  </section>
</template>

<style lang="scss" scoped>
@import '../style/components/index';

.field {
  width: 100%;
  padding: 12px 16px;
  font-weight: 300;
  font-size: 16px;
  line-height: 20px;
  color: #333333;
  border: 1px solid #cfdce3;
  box-sizing: border-box;

  &::placeholder {
    font-weight: 300;
    font-size: 16px;
    line-height: 20px;
    color: rgba(51, 51, 51, 0.3);
  }
}

.feedback {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-gap: 20px;

  h3 {
    margin: 60px 0 0 0;
  }

  header {
    grid-column: 2 / span 4;

    margin-top: 100px;
  }

  &-img {
    grid-column: 7 / -1;
    grid-row: 1 / 3;
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  &-form {
    grid-column: 2 / span 4;

    display: grid;
    grid-template-columns: repeat(6, 1fr);
    grid-column-gap: 24px;
    grid-row-gap: 6px;
    grid-template-areas:
      'title title name name surname surname'
      'email email email email email email'
      'phone phone phone phone phone phone'
      'policy policy policy subscribe subscribe subscribe'
      'submit submit submit . . .';
    margin-bottom: 90px;
    label {
      font-weight: 300;
      font-size: 12px;
      line-height: 18px;
      color: #333333;
    }
  }

  .titles {
    grid-area: title;
  }

  .name {
    grid-area: name;
  }

  .surname {
    grid-area: surname;
  }

  .email {
    grid-area: email;
  }

  .phone {
    grid-area: phone;
  }

  .policy {
    grid-area: policy;
    margin-top: 25px;
  }

  .subscribe {
    grid-area: subscribe;
    margin-top: 15px;
  }

  .submit {
    grid-area: submit;
  }
}
</style>