<script setup lang="ts">
import ButtonRed from '@/components/details/ButtonRed.vue'
import map1 from '@/components/images/map1.png'
import map2 from '@/components/images/map2.png'
</script>

<template>
  <section class="map">
    <h2 class="map__title">Our hills and valleys are like nothing you’ve seen.</h2>
    <p class="map__description">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce sit amet magna commodo, tempus
      dolor sit amet, laoreet elit. Donec mauris tortor.
    </p>
    <ButtonRed title="Learn More" class="map__btn-more" />
    <div class="map__images">
      <img class="map__image-left" :src="map1" alt="Изолинии слева" />
      <img class="map__image-right" :src="map2" alt="Изолинии справа" />
    </div>
  </section>
</template>

<style scoped lang="scss">
.map {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  position: relative;
  padding-top: 248px;
  padding-bottom: 255px;

  @media screen and (max-width: 719px) {
    padding: 176px 20px 120px;
  }

  &__image-left {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: auto;
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    z-index: -1;

    @media screen and (max-width: 1023px) {
      width: 150%;
    }

    @media screen and (max-width: 719px) {
      top: -226px;
      left: 130px;
      transform: rotate(40deg);
      transform-origin: top left;
      width: 280%;
      height: auto;
    }
  }

  &__image-right {
    position: absolute;
    bottom: 0;
    right: 0;
    width: 40.2%;
    height: auto;
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    z-index: -1;

    @media screen and (max-width: 1263px) {
      width: 60%;
    }

    @media screen and (max-width: 1023px) {
      width: 80%;
    }

    @media screen and (max-width: 719px) {
      width: 110%;
      height: auto;
    }
  }

  &__title {
    font-family: 'DMSans', sans-serif;
    font-size: 42px;
    font-weight: 700;
    line-height: 50px;
    text-align: center;
    max-width: 600px;
    margin-bottom: 33px;
    color: #000;

    @media screen and (max-width: 719px) {
      font-size: 40px;
      line-height: 46px;
      margin-bottom: 36px;
    }
  }

  &__description {
    font-family: 'DMSans', sans-serif;
    text-align: center;
    color: #6f7787;
    font-size: 18px;
    font-weight: 400;
    line-height: 28px;
    letter-spacing: 0.5px;
    margin-bottom: 37px;
    max-width: 470px;

    @media screen and (max-width: 719px) {
      font-size: 16px;
      line-height: 24px;
      margin-bottom: 40px;
    }
  }

  &__btn-more {
    width: 210px;
    height: 64px;
    @media screen and (max-width: 719px) {
      height: 73px;
      width: 100%;
    }
  }

  //&__image-left {
  //  position: absolute;
  //  top: 0;
  //  left: 0;
  //  width: 116%;
  //  z-index: -1;
  //}
  //
  //&__image-right {
  //  position: absolute;
  //  width: 100%;
  //  height: auto;
  //}
}
</style>
