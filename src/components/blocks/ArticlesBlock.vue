<script setup lang="ts">
import art from '../images/art1.png'
import ButtonLearnMore from '@/components/details/ButtonRed.vue'
</script>

<template>
  <section class="articles">
    <h2 class="articles__title">Articles</h2>
    <ul class="articles__list">
      <li class="articles__item articles__item_type-top">
        <img class="articles__img" :src="art" alt="Article image" />
        <div class="articles__content">
          <h3 class="articles__content-title">The walkways of Indonesia spellbind</h3>
          <p class="articles__description">
            Lorem ipsum dolor sit amet, consectetur adip iscing elit. Fusce commodo magna et libero
            mollis rhoncus.
          </p>
          <ButtonLearnMore title="Learn More" class="articles__btn" />
        </div>
      </li>
      <li class="articles__item articles__item_type-bottom">
        <img
          class="articles__img"
          src="https://images.unsplash.com/photo-1573834289156-f25cca91aa6c?q=80&w=2069&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
          alt="Article image"
        />
        <div class="articles__content articles__content_type-reverse">
          <h3 class="articles__content-title">Perfect beaches exude relaxation and fun</h3>
          <p class="articles__description">
            Lorem ipsum dolor sit amet, consectetur adip iscing elit. Fusce commodo magna et libero
            mollis rhoncus.
          </p>
          <ButtonLearnMore title="Learn More" class="articles__btn" />
        </div>
      </li>
    </ul>
  </section>
</template>

<style scoped lang="scss">
.articles {
  display: flex;
  flex-direction: column;
  align-items: center;
  //background-color: #010a20;

  &__title {
    display: none;
    opacity: 0;
  }

  &__list {
    display: flex;
    flex-direction: column;
    padding-left: 0;
    width: 100%;
  }

  &__item {
    display: flex;
    gap: 131px;
    padding: 205px 120px 0 340px;

    &:last-child {
      flex-direction: row-reverse;
      justify-content: start;
      padding-top: 190px;
      padding-left: 381px;
      padding-bottom: 305px;
    }

    &_type-top {
      background: linear-gradient(360deg, #010a20 0%, rgba(1, 10, 32, 0) 100%),
        url('../images/back2.png');
      background-size: cover;
      background-position: center;
    }

    &_type-bottom {
      background: linear-gradient(180deg, #010a20 0%, rgba(1, 10, 32, 0) 100%),
        url('../images/back1.png');
      background-size: cover;
      background-position: center;
    }
  }

  &__img {
    width: 630.34px;
    height: 460px;
    border-radius: 10px;
    object-position: center;
    object-fit: cover;
  }

  &__content {
    display: flex;
    flex-direction: column;
    text-align: start;
    padding: 57px 0;
    max-width: 479.5px;

    &_type-reverse {
      padding-top: 68px;
      padding-left: 4px;
    }
  }

  &__content-title {
    font-family: 'DMSans', sans-serif;
    font-size: 42px;
    font-weight: 700;
    line-height: 50px;
    text-align: left;
    color: #ffffff;
    margin-bottom: 23px;
  }

  &__description {
    font-family: 'DMSans', sans-serif;
    font-size: 18px;
    font-weight: 400;
    line-height: 28px;
    letter-spacing: 0.01em;
    margin-bottom: 33px;
    color: #e0e0e0;
    width: 420px;
  }

  &__btn {
    width: 179.81px;
  }
}
</style>
