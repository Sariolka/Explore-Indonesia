<script setup lang="ts">
import ButtonLearnMore from '@/components/details/ButtonRed.vue'
</script>

<template>
  <section class="plans">
    <h2 class="plans__title">Getting there</h2>
    <ul class="plans__list">
      <li class="plans__item"></li>
      <li class="plans__item"></li>
      <li class="plans__item">
        <ButtonLearnMore />
      </li>
    </ul>
  </section>
</template>

<style scoped lang="scss">
.plans {
  display: flex;
  flex-direction: column;
  padding: 100px 200px;
  background-color: #dce8f2;

  &__title {
    font-family: 'DMSans', sans-serif;
    font-size: 60px;
    font-weight: 700;
    line-height: 90px;
    color: #010a20;
  }
}
</style>
