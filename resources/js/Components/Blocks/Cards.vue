<template>
  <div class="cards">
    <div class="cards__container">
      <div class="cards__row grid grid-cols-3 xl:grid-cols-2 sm:grid-cols-1">
        <div class="cards__item">
          <div class="cards__body">
            <div class="cards__content">
              <div class="cards__title">Более 35 тыс</div>
              <div class="cards__text">выпускников школы</div>
            </div>
            <div class="cards__image">
              <img src="/images/key.svg" alt="Ключи">
            </div>
          </div>
        </div>
        <div class="cards__item">
          <div class="cards__body">
            <div class="cards__content">
              <div class="cards__title">Автопарк</div>
              <div class="cards__text">организации ежегодно обновляется</div>
            </div>
            <div class="cards__image">
              <img src="/images/cars.svg" alt="Машины">
            </div>
          </div>
        </div>
        <div class="cards__item xl:col-span-2 sm:col-span-1">
          <div class="cards__body">
            <div class="cards__content">
              <div class="cards__title">Рассрочка</div>
              <div class="cards__text">на вес курс первый взнос-1000р</div>
            </div>
            <div class="cards__image">
              <img src="/images/bank.svg" alt="Банки">
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import {Link} from '@inertiajs/inertia-vue3';

export default {
  components: {
    Link,
  },
}
</script>

<style lang="scss" scoped>

@import 'resources/css/colors.scss';

$cardheight: 169px;

.cards {
  margin-top: calc($cardheight * -1 + $cardheight / 2);

  &__row {
    gap: 32px;
  }

  &__item {
    margin: 0 auto;
    max-width: 365px;
    border: 7px solid $purple;
    border-radius: 5px;
    background: $white;
  }

  &__body {
    padding: 20px 24px;
    height: 100%;
    display: flex;
    justify-content: space-between;
  }

  &__title {
    margin-bottom: 5px;
    font-size: 30px;
  }

  &__text {
    font-size: 20px;
    max-width: 147px;
    line-height: 1.2;
  }

  &__content {
    padding: 0px 6px 0px 0px;

  }

  &__image {
    min-width: 90px;
    display: flex;
    justify-content: center;
    align-items: center;
    object-fit: contain;
  }
}

@media (max-width: 788px){
  .cards__text {
    margin-right: 10px;
  }
}

</style>
