<script setup lang="ts">
import ButtonRed from '@/components/details/ButtonRed.vue'
import HeroItem from '@/components/details/HeroItem.vue'
</script>

<template>
  <section class="hero">
    <header class="hero__header">
      <div class="hero__left-side">
        <img class="hero__logo" src="@/components/images/logo.svg" alt="Logo" />
        <a href="#" class="hero__link">destinations</a>
        <a href="#" class="hero__link">experiences</a>
        <a href="#" class="hero__link">about</a>
        <a href="#" class="hero__link">gallery</a>
      </div>
      <div class="hero__right-side">
        <button class="hero__btn hero__btn_type-search" aria-label="Search"></button>
        <button class="hero__btn hero__btn_type-menu" aria-label="Open menu"></button>
      </div>
    </header>
    <div class="hero__content">
      <div class="hero__wrapper">
        <div class="hero__line-up"></div>
        <div class="hero__line-down"></div>
      </div>
      <div class="hero__title-container">
        <h1 class="hero__title">explore indonesia</h1>
        <ButtonRed title="Start travelling" class="hero__btn-start" size="medium" />
      </div>
    </div>
    <div class="hero__footer">
      <div class="hero__social">
        <a href="#" class="hero__link-social">Fb</a>
        <a href="#" class="hero__link-social">In</a>
        <a href="#" class="hero__link-social">Tw</a>
      </div>
      <div class="hero__footer-container">
        <ul class="hero__list">
          <HeroItem
            title="Title here"
            number="01"
            description="Lorem ipsum dolor sit amet et amet ist ame."
            class="hero__li"
          />
          <HeroItem
            title="Title here"
            number="02"
            description="Lorem ipsum dolor sit amet et amet ist ame."
            class="hero__li"
          />
          <HeroItem
            title="Title here"
            number="03"
            description="Lorem ipsum dolor sit amet et amet ist ame."
            class="hero__li"
          />
        </ul>
        <div class="hero__video">
          <button class="hero__play"></button>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped lang="scss">
.hero {
  display: flex;
  flex-direction: column;
  background-image: url('@/components/images/hero.png');
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;

  &__header {
    display: flex;
    padding: 28px 140px 28px 25px;
    width: 100%;
    justify-content: space-between;
    margin-bottom: 110px;
  }

  &__left-side {
    display: flex;
    align-items: center;
    gap: 62px;
  }

  &__right-side {
    display: flex;
    align-items: start;
    gap: 35px;
    padding-top: 10px;
  }

  &__btn-start {
    width: 271px;
    height: 82px;
  }

  &__content {
    display: flex;
    align-items: start;
    margin-bottom: 195px;
  }

  &__wrapper {
    margin-right: 201px;
    display: flex;
    flex-direction: column;
    padding-left: 69px;
  }

  &__line-up {
    border-left: 4px solid #dd2242;
    box-shadow: 0 4px 4px 0 #00000073;
    height: 100px;
  }

  &__line-down {
    border-left: 2px solid #fff;
    box-shadow: 0 4px 4px 0 #00000073;
    height: 296px;
    margin-left: 1px;
  }

  &__btn {
    width: 24px;
    height: 24px;
    border: none;
    background-color: transparent;
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    cursor: pointer;

    &_type-search {
      width: 30px;
      height: 30px;
      background-image: url('@/components/icons/search.svg');
    }
    &_type-menu {
      background-image: url('@/components/icons/menu.svg');
    }
  }

  &__link {
    font-family: 'DMSans', sans-serif;
    font-size: 18px;
    font-weight: 700;
    line-height: 23.44px;
    color: #fff;
    text-transform: uppercase;
    text-decoration: none;
    margin-bottom: 3px;
    padding-left: 0;
  }

  &__link-social {
    font-family: 'DMSans', sans-serif;
    font-size: 16px;
    font-weight: 700;
    line-height: 20.83px;
    color: #fff;
    text-decoration: none;
    margin-left: 38.5px;
  }

  &__title-container {
    display: flex;
    flex-direction: column;
    align-items: start;
  }

  &__title {
    font-family: 'DMSans', sans-serif;
    font-size: 120px;
    font-weight: 900;
    line-height: 130px;
    text-align: left;
    color: #fff;
    text-transform: uppercase;
    max-width: 627.33px;
    margin-top: 30px;
    margin-bottom: 20px;
  }

  &__list {
    background-color: #000;
    opacity: 60%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 67%;
    padding: 40px 130px 40px 68px;
  }
  &__video {
    position: relative;
    background-image: url('@/components/images/hero2.png');
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    z-index: 1;
    width: 417px;
    aspect-ratio: 417/254;
    height: auto;
  }
  &__play {
    position: absolute;
    top: 34%;
    left: 41.5%;
    background-image: url('@/components/icons/play.svg');
    background-repeat: no-repeat;
    background-position: center;
    background-size: 30%;
    border: none;
    cursor: pointer;
    padding: 39px;
    border-radius: 50%;
    background-color: #fff;
    color: #000;
    @media screen and (max-width: 719px) {
      padding: 33.5px;
      top: 31%;
      left: 40%;
    }
  }

  &__footer-container {
    display: flex;
    align-items: end;
    justify-content: end;
    width: 100%;
  }

  &__footer {
    display: flex;
    align-items: end;
  }

  &__social {
    transform: rotate(-90deg);
    margin-bottom: 5px;
    width: 21px;
    margin-left: 57px;
  }
}
</style>
