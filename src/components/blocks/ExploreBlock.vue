<script setup lang="ts">
import ByTheNumbersBlock from '@/components/blocks/ByTheNumbersBlock.vue'
import 'vue3-carousel/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'
import img1 from '@/components/images/1.jpg'
import img2 from '@/components/images/2.jpg'
import img3 from '@/components/images/3.jpg'
import img4 from '@/components/images/4.jpg'
import img5 from '@/components/images/5.jpg'
const data = [img1, img4, img5, img2, img3]
const carouselConfig = {
  itemsToShow: 3,
  wrapAround: true,
}
</script>

<template>
  <section class="explore">
    <Carousel v-bind="carouselConfig">
      <Slide v-for="slide in data" :key="slide">
        <img class="carousel__item" :src="slide" alt="Picture" />
      </Slide>
      <template #addons>
        <Navigation />
        <Pagination />
      </template>
    </Carousel>
    <ByTheNumbersBlock />
  </section>
</template>

<style scoped lang="scss">
.explore {
  background-image: url('../images/explore.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  height: 2207px;
  background-position: center;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
</style>
<style scoped>
.carousel {
  width: 80%;
  margin-left: auto;
  margin-right: auto;
}
.carousel__slide {
  height: 310px;
}
.carousel__item {
  height: 257px;
  width: 405px;
  background-color: #642afb;
  color: white;
  font-size: 20px;
  border-radius: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
}

.carousel__prev,
.carousel__next {
  box-sizing: content-box;
  border: 5px solid red;
}
</style>
