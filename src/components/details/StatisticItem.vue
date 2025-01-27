<script setup lang="ts">
const props = defineProps<{
  title: string
  text: string
}>()
</script>

<template>
  <li class="statistic-item">
    <span class="statistic-item__counter">{{ title }}</span>
    <p class="statistic-item__description">{{ text }}</p>
  </li>
</template>

<style scoped lang="scss">
.statistic-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  gap: 18px;

  @media screen and (max-width: 1279px) {
    gap: 11px;
  }

  &__counter {
    font-family: 'DMSans', sans-serif;
    font-size: 42.14px;
    font-weight: 700;
    line-height: 49.16px;
    letter-spacing: 0.38626033067703247px;
    color: #dd2242;
    @media screen and (max-width: 1279px) {
      font-size: 40px;
      line-height: 46px;
      letter-spacing: 0;
    }
  }

  &__description {
    font-family: 'DMSans', sans-serif;
    font-size: 18px;
    font-weight: 400;
    line-height: 28px;
    letter-spacing: 0.5px;
    color: #e0e0e0;

    @media screen and (max-width: 1279px) {
      font-size: 16px;
      line-height: 24px;
    }
  }
}
</style>
