<script setup lang="ts">
import art from '../images/art1.png'
import ButtonLearnMore from '@/components/details/ButtonRed.vue'
</script>

<template>
  <section class="articles">
    <h2 class="articles__title">Articles</h2>
    <ul class="articles__list">
      <li class="articles__item articles__item_type-top">
        <div class="articles__inner">
          <img class="articles__img" :src="art" alt="Article image" />
          <div class="articles__content">
            <h3 class="articles__content-title">The walkways of Indonesia spellbind</h3>
            <p class="articles__description">
              Lorem ipsum dolor sit amet, conse ctetur adip iscing elit. Fusce commodo magna et
              libero mollis rhoncus.
            </p>
            <ButtonLearnMore title="Learn More" class="articles__btn" />
          </div>
        </div>
      </li>
      <li class="articles__item articles__item_type-bottom">
        <div class="articles__inner articles__inner_type-reverse">
          <div class="articles__content articles__content_type-reverse">
            <h3 class="articles__content-title">Perfect beaches exude relaxation and fun</h3>
            <p class="articles__description">
              Lorem ipsum dolor sit amet, conse ctetur adip iscing elit. Fusce commodo magna et
              libero mollis rhoncus.
            </p>
            <ButtonLearnMore title="Learn More" class="articles__btn" />
          </div>
          <img
            class="articles__img"
            src="https://images.unsplash.com/photo-1573834289156-f25cca91aa6c?q=80&w=2069&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
            alt="Article image"
          />
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
  background-color: #010a20;
  cursor: default;

  @media screen and (max-width: 1023px) {
    padding-left: 30.5px;
    padding-right: 30.5px;
  }

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
    padding-top: 205px;
    justify-content: center;

    &:last-child {
      padding-top: 190px;
      padding-bottom: 305px;

      @media screen and (max-width: 1279px) {
        padding-top: 52px;
        padding-bottom: 40px;
      }
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
    @media screen and (max-width: 1279px) {
      padding-right: 20px;
      padding-left: 20px;
      padding-top: 42px;
    }
    @media screen and (max-width: 1023px) {
      width: 100%;
    }
  }

  &__inner {
    display: grid;
    grid-template-columns: auto 479.5px;
    gap: 131px;

    @media screen and (max-width: 1279px) {
      gap: 35px;
      align-items: center;
    }
    @media screen and (max-width: 1023px) {
      display: flex;
      flex-direction: column;
      width: 100%;
    }
  }

  &__inner_type-reverse {
    display: grid;
    justify-content: start;
    grid-template-columns: 479.5px auto;

    @media screen and (max-width: 1279px) {
      align-items: center;
    }
    @media screen and (max-width: 1023px) {
      display: flex;
      flex-direction: column-reverse;
      width: 100%;
    }
  }

  &__img {
    max-width: 630px;
    width: 100%;
    height: auto;
    aspect-ratio: 63/46;
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

    @media screen and (max-width: 719px) {
      padding-top: 0;
      padding-bottom: 0;
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

    @media screen and (max-width: 1023px) {
      font-size: 40px;
      line-height: 47px;
    }

    @media screen and (max-width: 719px) {
      margin-bottom: 20px;
    }
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
    text-align: left;

    @media screen and (max-width: 1023px) {
      font-size: 16px;
      line-height: 24px;
      letter-spacing: 0.5px;
      width: 100%;
      margin-bottom: 32px;
    }
  }

  &__btn {
    width: 179.81px;
    height: 59px;
    @media screen and (max-width: 719px) {
      width: 100%;
      height: 72px;
    }
  }
}
</style>
