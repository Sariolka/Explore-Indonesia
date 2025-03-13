<script setup lang="ts">
const props = defineProps<{
  number: string;
  title: string;
  description: string;
}>();
</script>

<template>
  <li class="hero-item">
    <span class="hero-item__number">{{ number }}</span>
    <h2 class="hero-item__title">{{ title }}</h2>
    <p class="hero-item__description">{{ description }}</p>
  </li>
</template>

<style scoped lang="scss">
.hero-item {
  display: flex;
  flex-direction: column;
  width: 210px;

  &__number {
    font-family: 'Roboto', sans-serif;
    font-size: 16px;
    font-weight: 900;
    line-height: 18.75px;
    text-align: left;
    color: #dd2242;
    margin-bottom: 11px;

    @media screen and (max-width: 1023px) {
      margin-bottom: 5px;
    }
  }

  &__title {
    font-family: 'DMSans', sans-serif;
    font-size: 26.41px;
    font-weight: 700;
    line-height: 40.08px;
    text-align: left;
    color: #fff;
  }

  &__description {
    font-family: 'DMSans', sans-serif;
    font-size: 18px;
    font-weight: 400;
    line-height: 28px;
    letter-spacing: 0.5px;
    color: #939393;

    @media screen and (max-width: 1279px) {
      font-size: 16px;
      line-height: 24px;
    }
  }
}
</style>
