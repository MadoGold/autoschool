<template>
  <div class="contact-us">
    <div class="contact-us__container">
      <h2 class="contact-us__title title">Остались вопросы?</h2>
      <div class="contact-us__body">
        <div class="contact-us__address">
          <div class="contact-us__place">
            <p>Мы находимся по адресу:</p>
            <p>метро Автово</p>
            <p>Позвоните нам:</p>
            <p><a href="tel:+74951234567">+7 (495) 123-45-67</a></p>
            <p>Ежедневно с 8;00  до  18:00</p>
            <p>Или напишите нам:</p>
            <p><a href="mailto:pochta@pochta.ru">pochta@pochta.ru</a></p>
          </div>
          <div class="contact-us__map">
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d8010.78644671064!2d30.254637354121165!3d59.87078365962435!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x46963a891f1a7441%3A0xd8ea3c584c2ecf1d!2z0JDQstGC0L7QstC-LCDQodCw0L3QutGCLdCf0LXRgtC10YDQsdGD0YDQsywgMTk4MDk2!5e0!3m2!1sru!2sru!4v1649658523439!5m2!1sru!2sru" width="100%" height="100%" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
          </div>
        </div>
        <form class="contact-us__form form" action="#" method="post">
          <ul class="form__list grid grid-cols-1 grid-rows-4 gap-6 h-full">
            <li class="form__item">
              <input type="text" id="name" placeholder="Ваше имя" name="user_name">
            </li>
            <li class="form__item">
              <InputPhone placeholder="Ваш телефон" name="user_tel" />
            </li>
            <li class="form__item">
              <input type="email" id="mail" placeholder="Ваша почта" name="user_mail">
            </li>
            <li class="form__item">
              <Button class="form__button">Записаться в автошколу</Button>
            </li>
            <li class="form__item">
              <div class="text-center">
                <p class="contact-us__text mb-2">Нажимая на кнопку, Вы соглашаетесь
                  с условиями</p>
                <a href="http://www.consultant.ru/document/cons_doc_LAW_61801/315f051396c88f1e4f827ba3f2ae313d999a1873/" class="contact-us__link" target="_blank">обработки персональных данных</a>
              </div>
            </li>
          </ul>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
import Button from '@/Components/Button';
import InputPhone from '@/Components/InputPhone';

export default {
  components: {
    Button,
    InputPhone,
  },
}

</script>

<style lang="scss" scoped>

@import 'resources/css/colors.scss';

.contact-us {
  padding: 50px 0 100px 0;

  @media (max-width: 1200px) {
    padding: 50px 0;
  }

  &__title {
    margin-left: 130px;
    font-size: 40px;

    @media (max-width: 1200px) {
      margin: 0;
      text-align: center;
    }
  }

  &__body {
    display: flex;
    justify-content: space-between;
    margin-top: 35px;
    @media (max-width: 1200px) {
      flex-direction: column-reverse;
    }
  }

  &__address {
    position: relative;
    height: 100%;
  }

  &__map {
    padding-left: 105px;

    & iframe {
      border: 1px solid $purple;
      height: 426px;
      width: 590px;

      @media (max-width: 1200px) {
        width: 100%;
      }
    }
    @media (max-width: 1200px) {
      padding-left: 0;
    }
  }

  &__place {
    padding: 50px 15px 32px 15px;
    position: absolute;
    text-align: center;
    transform: translateY(25%);
    top: 0;
    left: 0;
    background-color: $white;
    border: 1.5px solid $purple;

    @media (max-width: 800px) {
      transform: none;
    }

    & p {
      font-family: Nunito, sans-serif;
      font-size: 18px;
      font-weight: 700;

      &:not(:last-child) {
        margin-bottom: 15px;
        @media (max-width: 800px) {
          margin-bottom: 8px;
        }
      }
      &:nth-child(2n) {
        color: $purple;
      }
      & a:hover {
        text-decoration: underline;
      }
    }

    @media (max-width: 800px) {
      padding: 25px 10px 16px 10px;
      margin-bottom: 15px;
      position: static;
    }
  }
  &__link {
    color: $purple;
    &:hover {
      text-decoration: underline;
    }
  }
}

.form {
  &__item {
    &:not(:last-child) {
      box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
      border-radius: 23px;
      border: none;
    }

    & input {
      font-family: Nunito, sans-serif;
      width: 100%;
      height: 100%;
      background-color: $gray;
      border: none;
      border-radius: 23px;
      font-size: 25px;
      font-weight: 600;

      &:focus {
        border: 1px solid $purple;
      }

      &:valid {
        padding: 0 28px;
      }

      &::placeholder {
        color: $black;
        opacity: 0.5;
        font-weight: 600;
        font-size: 25px;
      }
    }
  }

  &__button {
    height: 100%;
    width: 100%;
  }

  @media (max-width: 1200px) {
    margin-bottom: 20px;
  }
}

</style>
