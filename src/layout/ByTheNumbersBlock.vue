<script setup lang="ts">
import StatisticItem from '@/components/StatisticItem.vue';

const data = [
  {
    title: '100+',
    text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce commodo magna et libero.',
  },
  {
    title: '43,000+',
    text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce commodo.',
  },
  {
    title: '30+',
    text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce commodo magna et libero.',
  },
];
</script>

<template>
  <section class="analytic">
    <h2 class="analytic__header">By The Numbers</h2>
    <p class="analytic__description">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce commodo magna et libero.Lorem
      ipsum dolor sit amet, consectetur adipiscing elit.
    </p>
    <ul class="analytic__list">
      <StatisticItem
        v-for="(li, index) in data"
        :key="index"
        class="analytic__item"
        :class="{ 'analytic__item_type-width': li.title === '43,000+' }"
        :text="li.text"
        :title="li.title"
      />
    </ul>
  </section>
</template>

<style scoped lang="scss">
.analytic {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: #020c21;
  opacity: 90%;
  padding: 182px 200px 210px;
  cursor: default;

  @media screen and (max-width: 1023px) {
    padding: 52px 30.5px 60px;
  }

  &__header {
    font-family: 'DMSans', sans-serif;
    font-size: 60px;
    font-weight: 700;
    line-height: 90px;
    color: #ffffff;
    margin-bottom: 18px;
    text-align: center;

    @media screen and (max-width: 1023px) {
      font-size: 40px;
      line-height: 46px;
      margin-bottom: 37px;
    }
  }

  &__description {
    font-family: 'DMSans', sans-serif;
    font-size: 18px;
    font-weight: 400;
    line-height: 28px;
    letter-spacing: 0.5px;
    color: #e0e0e0;
    width: 484px;
    text-align: center;
    margin-bottom: 57px;
    @media screen and (max-width: 1023px) {
      font-size: 16px;
      line-height: 24px;
      width: auto;
      margin-bottom: 61px;
    }
  }

  &__list {
    display: flex;
    padding-left: 0;

    @media screen and (max-width: 1023px) {
      gap: 20px;
      flex-direction: column;
      align-items: center;
    }

    @media screen and (max-width: 719px) {
      gap: 0;
    }
  }

  &__item {
    width: 300px;
    @media screen and (max-width: 330px) {
      width: 250px;
    }
    &:first-child {
      margin-right: 150px;
      @media screen and (max-width: 1279px) {
        margin-right: 0;
      }
      @media screen and (max-width: 1023px) {
        margin-bottom: 80px;
      }
    }

    &:nth-child(2) {
      margin-right: 105px;
      @media screen and (max-width: 1279px) {
        margin-right: 0;
      }
      @media screen and (max-width: 1023px) {
        margin-bottom: 35px;
      }
    }

    &_type-width {
      width: 380px;
      @media screen and (max-width: 719px) {
        width: 300px;
      }
      @media screen and (max-width: 330px) {
        width: 250px;
      }
    }
  }
}
</style>
