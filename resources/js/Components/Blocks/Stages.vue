<template>
  <div class="stages">
    <div class="stages__container">
      <div class="stages__content">
        <h2 class="stages__title">Этапы обучения</h2>
        <div class="stages__items grid grid-cols-4 xl:grid-cols-2">
          <div class="stages__item" v-for="(stage, index) in stages" :key="index">
            <div class="stages__body">
              <div class="stages__number">
                <div class="stages__number-text"> {{ index + 1 }} </div>
                <div class="stages__img" :style="['background-image: url(images/bagpack-' + index + '.svg)']"></div>
              </div>
              <div class="stages__text">
              {{ stage.text}}
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'stagesItem',
  data() {
    return {
      stages: [
        {
          text: 'Подать документы',
        },
        {
          text: 'Подать документы',
        },
        {
          text: 'Подать документы',
        },
        {
          text: 'Подать документы',
        },
      ],
    }
  },

}

</script>

<style lang='scss' scoped>

@import 'resources/css/colors.scss';

.stages {
  padding-bottom: 43px;
  border-bottom: 3px dashed $purple;

  &__title {
    display: inline-block;
    position: relative;
    margin-bottom: 100px;
    font-size: 55px;

    &::after {
      content: '';
      position: absolute;
      top: 45px;
      right: -200px;
      background-image: url('/images/arrow.svg');
      background-size: contain;
      background-repeat: no-repeat;
      padding-right: 185px;
      padding-top: 35px;
    }
  }

  &__items {
    gap: 50px;
    @media (max-width: 640px) {
      gap: 20px;
    }
  }

  &__item {
    border: 3px solid $purple;
    box-shadow: 0px 0px 20px 0px rgba(0, 0, 0, 0.2);
    border-radius: 23px;
  }

  &__body {
    padding: 35px 15px;
    @media (max-width: 640px) {
      padding: 25px 10px;
    }
  }

  &__number {
    display: flex;
    justify-content: space-between;
  }

  &__number-text {
    margin-right: 10px;
    font-size: 110px;
    color: $purple;
    @media (max-width: 540px) {
      font-size: 70px;
    }
  }

  &__img {
    margin-right: 10px;
    padding-right: 117px;
    display: inline-block;
    background-repeat: no-repeat;
    background-size: contain;
    @media (max-width: 540px) {
      padding-right: 100px;
    }
	}

  &__text {
    font-size: 23px;
    margin-top: 25px;

    @media (max-width: 640px) {
      margin-top: 10px;
    }

    & span{
      color: $purple;
    }
  }
}

@media (max-width: 1200px){
  .stages__items {
    flex-wrap: wrap;
    justify-content: space-around;
  }

}

@media (max-width: 955px){

  .stages__title {
    margin-bottom: 60px;
  }

}

@media (max-width: 640px){

  .stages__title::after {
      display: none;
  }

  .stages__title {
    margin-bottom: 30px;
    align-content: center;
    padding-bottom: 3px;
    font-size: 40px;
  }
}

</style>
