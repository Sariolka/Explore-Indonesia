<script setup lang="ts">
const props = defineProps<{
  image: string;
  title: string;
  description: string;
}>();
</script>

<template>
  <div class="card">
    <div class="card__video-container">
      <img class="card__video" :src="image" :alt="title" />
      <button class="card__btn" aria-label="play"></button>
    </div>

    <div class="card__content">
      <h3 class="card__title">{{ title }}</h3>
      <p class="card__description">{{ description }}</p>
    </div>
  </div>
</template>

<style scoped lang="scss">
.card {
  display: flex;
  gap: 50px;

  @media screen and (max-width: 1366px) {
    flex-direction: column;
    align-items: center;
    gap: 29px;
  }

  &__video-container {
    position: relative;
  }

  &__video {
    max-width: 233px;
    aspect-ratio: 233/151;
    height: auto;
    border-radius: 5px;
    object-fit: cover;

    @media screen and (max-width: 1366px) {
      max-width: 314px;
      aspect-ratio: 314/176;
    }

    @media screen and (max-width: 330px) {
      max-width: 270px;
      aspect-ratio: 314/176;
    }
  }

  &__btn {
    position: absolute;
    top: 70px;
    left: 50%;
    background-image: url('@/images/icons/play.svg');
    width: 16px;
    height: 18px;
    background-color: transparent;
    border: none;
    cursor: pointer;

    @media screen and (max-width: 1366px) {
      top: 80px;
    }
  }

  &__content {
    display: flex;
    flex-direction: column;
    justify-content: start;
    align-items: start;
    max-width: 336px;
    gap: 24px;
    @media screen and (max-width: 1366px) {
      text-align: center;
      align-items: center;
      gap: 15px;
    }
  }

  &__title {
    font-family: 'DMSans', sans-serif;
    font-size: 18px;
    font-weight: 700;
    line-height: 27px;
    color: #ffffff;
    @media screen and (max-width: 1366px) {
      font-size: 22px;
      line-height: 44px;
    }
  }

  &__description {
    font-family: 'DMSans', sans-serif;
    font-size: 18px;
    font-weight: 400;
    line-height: 28px;
    color: #ffffff;
    opacity: 70%;
    @media screen and (max-width: 1366px) {
      font-size: 16px;
      line-height: 24px;
      text-indent: 15px;
    }
  }
}
</style>
