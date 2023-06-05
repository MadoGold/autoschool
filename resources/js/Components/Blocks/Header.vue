<template>
  <header class="header">
    <div class="header__container">
      <div class="header__row">
        <Link class="header__logo h-full">
          <BreezeApplicationLogo/>
        </Link>
        <nav class="header__nav nav">
          <ul class="nav__list">
            <li class="nav__item"><Button class="nav__item-btn"
              onclick='window.scrollTo({top: (document.getElementById("categories").offsetTop - 110), behavior: "smooth"});'>Выбор категории</Button></li>
            <li class="nav__item"><Button class="nav__item-btn"
              onclick='window.scrollTo({top: (document.getElementById("stages").offsetTop - 110), behavior: "smooth"});'>Обучение</Button></li>
            <li class="nav__item"><Button class="nav__item-btn"
              onclick='window.scrollTo({top: (document.getElementById("contact-us").offsetTop - 110), behavior: "smooth"});'>Контакты</Button></li>
          </ul>
        </nav>
        <Button class="header__button">Вход</Button>
      </div>
    </div>
  </header>
</template>

<script>
import {Link} from '@inertiajs/inertia-vue3';
import BreezeApplicationLogo from '@/Components/ApplicationLogo.vue';
import Button from '@/Components/Button.vue';

export default {
  components: {
    BreezeApplicationLogo,
    Link,
    Button,
  },
}
</script>

<style lang="scss" scoped>

@import 'resources/css/colors.scss';

.header {
  padding: 28px 0;
  width: 100vw;
  position: fixed;
  background-color: $purple-opacity;
  backdrop-filter: blur(3px);
  z-index: 10;

  @media (max-width: 670px) {
    padding: 14px 0;
  }
}

.header__row {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.nav__list {
  display: flex;
  align-items: center;
}

.nav__item:not(:last-child) {
  margin-right: 35px;
}

.nav__item-btn {
  padding: 0;
  background-color: transparent;
  font-size: 23px;
  color: $white;
  transition: color .3s ease;

  &:hover {
    color: $yellow;
    transform: none;
  }
}

.header__button {
  padding: 12px 40px;
  background-color: $white;
  color: $purple;
  box-shadow: 0 4px 4px rgba(0, 0, 0, 0.25)
}

@media (max-width: 955px){
    .header__logo {
      display: none;
    }

    .nav__list {
      margin-left: 7px;
      flex-wrap: wrap;
    }

    .header__button {
      margin-left: 20px;
    }

    .nav__item:last-child {
      margin: 10px auto 0;
    }

    .nav__item {
      margin-top: 10px;
    }
    .header__button {
      margin: 0 10px 0 auto;
    }
    .header__container {
      width: 100%;
    }

    .header__button {
      margin-left: 3px;
    }

}

@media (max-width: 490px){
  .header {
    width: 100%;
  }

  .nav__item:last-child {
      margin: 10px 0 0;
  }

  .nav__item:first-child {
    flex-wrap: nowrap;
  }

  .header__nav {
    width: 90%;
  }

  .header__container {
    margin: 0 auto;
  }
}
</style>
