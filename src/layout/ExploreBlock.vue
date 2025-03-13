<script setup lang="ts">
import ByTheNumbersBlock from '@/layout/ByTheNumbersBlock.vue';
import 'vue3-carousel/carousel.css';
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel';
import img1 from '@/images/1.jpg';
import img2 from '@/images/2.jpg';
import img3 from '@/images/3.jpg';
import img4 from '@/images/4.jpg';
import img5 from '@/images/5.jpg';
const data = [img1, img4, img5, img2, img3];
const carouselConfig = {
  itemsToShow: 3,
  wrapAround: false,
  breakpoints: {
    1920: {
      itemsToShow: 3,
    },
    1023: {
      itemsToShow: 2,
    },
    300: {
      itemsToShow: 1,
    },
  },
};
</script>

<template>
  <section class="explore">
    <div class="explore__head">
      <h2 class="explore__title">Explore Our Secrets</h2>
      <Carousel v-bind="carouselConfig">
        <Slide v-for="slide in data" :key="slide">
          <img class="carousel__item" :src="slide" alt="Picture" />
        </Slide>
        <template #addons>
          <Navigation />
          <Pagination />
        </template>
      </Carousel>
    </div>

    <ByTheNumbersBlock />
  </section>
</template>

<style scoped lang="scss">
.explore {
  background-image: url('@/images/explore.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  height: 2207px;
  background-position: center;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding-top: 116px;

  @media screen and (max-width: 819px) {
    padding-top: 30px;
  }

  &__title {
    font-family: 'DMSans', sans-serif;
    font-size: 50px;
    font-weight: 700;
    line-height: 75px;
    text-align: center;
    color: #010a20;
    margin-bottom: 0;

    @media screen and (max-width: 819px) {
      font-size: 40px;
      line-height: 46px;
    }
  }
}
.carousel {
  width: 70%;
  margin-left: auto;
  margin-right: auto;

  @media screen and (max-width: 819px) {
    width: 98%;
  }

  &::v-deep(.carousel__pagination) {
    gap: 10px;
  }

  &::v-deep(.carousel__pagination-button) {
    background-color: #85a3b2;
    border-radius: 50%;
    width: 19px;
    height: 19px;
    margin-top: 0;
    margin-bottom: 0;

    @media screen and (max-width: 1023px) {
      width: 16.48px;
      height: 16.48px;
    }
  }

  &::v-deep(.carousel__pagination-button--active) {
    background-color: #dd2242;
    border-radius: 60px;
    width: 50px;
    height: 19px;
    margin: 0;

    @media screen and (max-width: 1023px) {
      width: 43.37px;
      height: 16.48px;
    }
  }
  &::v-deep(.carousel__prev) {
    left: -6%;
    height: 45px;

    @media screen and (max-width: 819px) {
      left: -6px;
    }

    @media screen and (max-width: 330px) {
      left: 0;
    }
  }

  &::v-deep(.carousel__icon) {
    width: 1em;
    height: 1.2em;
    color: #020b20;
  }

  &::v-deep(.carousel__next) {
    left: 102%;
    height: 45px;
    @media screen and (max-width: 819px) {
      left: 88%;
    }

    @media screen and (max-width: 330px) {
      left: 83%;
    }
  }
}
.carousel__slide {
  height: 325px;
  @media screen and (max-width: 819px) {
    height: 270px;
  }
}
.carousel__item {
  height: 257px;
  width: 405px;
  object-fit: cover;
  object-position: center 15%;
  border: none;
  color: white;
  font-size: 20px;
  border-radius: 10px;
  display: flex;
  justify-content: center;
  align-items: center;

  @media screen and (max-width: 1300px) {
    width: 314px;
    height: 200px;
  }

  @media screen and (max-width: 479px) {
    width: 250px;
  }
}
</style>
