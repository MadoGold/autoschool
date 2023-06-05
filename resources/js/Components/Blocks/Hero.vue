<template>
  <div class="hero">
    <div class="hero__container">
      <div class="hero__body">
        <h1 class="hero__title title">Научитесь водить автомобиль и получите права уже через 3 месяца </h1>
        <Button onclick='window.scrollTo({top: (document.getElementById("contact-us").offsetTop - 93), behavior: "smooth"});' class="hero__button">Записаться в автошколу</Button>
      </div>
    </div>
  </div>
</template>

<script>
import Button from '@/Components/Button';

export default {
  components: {
    Button,
  },
}

</script>

<style lang="scss" scoped>

@import 'resources/css/colors.scss';

.hero {
  padding: 173px 0px 154px 0px;
  background-image: url('/images/Xyiday.png');
  background-repeat: no-repeat;
  background-position: right -165px bottom 30px;
  background-size: 55%;
  background-color: $purple;

  @media (max-width: 1200px) {
    background-size: 75%;
    background-position: right -165px center;
  }

  @media (max-width: 820px) {
    background-image: none;
  }

  &__title {
    line-height: 1.27;
    max-width: 700px;
    padding: 0px 0px 67px 0px;
    font-size: 55px;
    font-weight: 700;
    color: $white;

    @media (max-width: 1200px) {
      max-width: 500px;
    }

    @media (max-width: 820px) {
      max-width: 700px;
      margin: 0 auto;
      text-align: center;
    }

    @media (max-width: 640px) {
      font-size: 36px;
    }
  }

  &__button {
    margin: 0px 0px 0px 78px;
    padding: 25px;
    font-size: 24px;
    color: $black;
    background-color: $yellow;

    @media (max-width: 820px) {
      display: block;
      margin: 0 auto;

    }
  }
}

</style>
