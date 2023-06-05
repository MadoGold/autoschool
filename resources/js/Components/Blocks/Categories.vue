<template>
  <div class="categories">
    <div class="categories__container">
      <div class="categories__body">
        <Button class="categories__button tab">Категория В</Button>
          <div class="categories__item flex">
            Теория<div class="flex-auto border-dotted border-black border-b-6 mb-[8px]"></div>5000₽
          </div>
          <div class="categories__item flex">
            Вождение<div class="flex-auto border-dotted border-black border-b-6 mb-[8px]"></div>1000₽/час
          </div>
        <Button class="categories__button" onclick='window.scrollTo({top: (document.getElementById("contact-us").offsetTop - 110), behavior: "smooth"});'>Записаться в автошколу</Button>
      </div>
      <div class="categories__image"></div>
    </div>
  </div>
</template>

<script>
import Button from '@/Components/Button.vue';

export default {
  components: {
    Button,
  },
}

</script>

<style lang="scss" scoped>

@import 'resources/css/colors.scss';

.categories {
  padding: 61px 0px 100px 0px;

  &__container {
    display: flex;
    justify-content: space-between;
  }

  &__body {
    min-height: 420px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    @media (max-width: 1200px) {
      min-height: 380px;
    }
  }

  &__button {
    font-size: 32px;
    padding: 32px 50px;
  }

  &__item {
    font-size: 36px;
    margin-bottom: 25px;
  }

  &__image {
    flex: 0 1 40%;
    background-image: url('/images/supercarcircles.png');
    background-repeat: no-repeat;
    background-position: right center;
    background-size: contain;
  }
}

.tab {
  padding: 24px 50px;
  font-size: 36px;
  cursor: default;
  margin-bottom: 25px;
  &:hover {
    transform: none;
  }
}

@media (max-width: 840px) {
  .categories {
    padding-bottom: 60px;
  }

  .categories__image {
    display: none;
  }

  .categories__body {
    margin: 0px auto;
  }

}

@media (max-width: 550px) {
  .categories__button {
    font-size: 28px;
    padding: 32px 30px;
  }
}

</style>

