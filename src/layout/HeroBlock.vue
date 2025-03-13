<script setup lang="ts">
import ButtonRed from '@/components/ButtonRed.vue';
import HeroItem from '@/components/HeroItem.vue';
</script>

<template>
  <header class="hero">
    <div class="hero__header">
      <div class="hero__left-side">
        <div class="hero__logo-container">
          <img class="hero__logo" src="../images/logo.svg" alt="Logo" />
          <p class="hero__text">explore indonesia</p>
        </div>

        <nav class="hero__links">
          <a href="#" class="hero__link">destinations</a>
          <a href="#" class="hero__link">experiences</a>
          <a href="#" class="hero__link">about</a>
          <a href="#" class="hero__link">gallery</a>
        </nav>
      </div>
      <div class="hero__right-side">
        <button class="hero__btn hero__btn_type-search" aria-label="Search"></button>
        <button class="hero__btn hero__btn_type-menu" aria-label="Open menu"></button>
      </div>
    </div>
    <div class="hero__content">
      <div class="hero__wrapper">
        <div class="hero__line-up"></div>
        <div class="hero__line-down"></div>
        <span class="hero__wrapper-count">01</span>
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
          <button class="hero__play" aria-label="play"></button>
        </div>
      </div>
    </div>
  </header>
</template>

<style scoped lang="scss">
.hero {
  display: flex;
  flex-direction: column;
  background: linear-gradient(215.79deg, rgba(0, 0, 0, 0.31) 29.66%, rgba(0, 0, 0, 0.29) 84.2%),
    url('@/images/hero.png');
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;

  &__header {
    display: flex;
    padding: 28px 135px 28px 27px;
    width: 100%;
    justify-content: space-between;
    margin-bottom: 126px;
    @media screen and (max-width: 1023px) {
      margin-bottom: 55px;
    }

    @media screen and (max-width: 719px) {
      padding: 50px 35px 28px 20px;
      margin-bottom: 0;
    }
    @media screen and (max-width: 479px) {
      padding: 50px 10px 28px 5px;
      margin-bottom: 0;
    }
  }

  &__logo-container {
    display: flex;
    margin-left: 10px;
    align-items: end;
    gap: 7px;
    max-width: 166px;
    background: linear-gradient(180deg, rgba(1, 132, 149, 0) 7.41%, #018394 83.33%);
  }

  &__logo {
    @media screen and (max-width: 1023px) {
      width: 21.32px;
    }
  }

  &__text {
    font-family: 'Roboto', sans-serif;
    font-size: 23.96px;
    font-weight: 900;
    line-height: 19.29px;
    letter-spacing: 0.31527093052864075px;
    color: #fff;
    text-transform: uppercase;
    @media screen and (max-width: 1023px) {
      font-size: 20.84px;
      line-height: 16.78px;
      letter-spacing: 0.27px;
    }
  }

  &__left-side {
    display: flex;
    align-items: end;
    gap: 71px;

    @media screen and (max-width: 1279px) {
      gap: 20px;
    }
  }

  &__links {
    display: flex;
    align-items: end;
    gap: 62px;

    @media screen and (max-width: 1279px) {
      gap: 20px;
    }

    @media screen and (max-width: 1023px) {
      display: none;
    }
  }

  &__right-side {
    display: flex;
    align-items: start;
    gap: 39px;
    padding-top: 8px;

    @media screen and (max-width: 719px) {
      gap: 25px;
    }
  }

  &__btn-start {
    width: 271px;
    height: 82px;

    @media screen and (max-width: 719px) {
      width: 100%;
      height: 59px;
    }
  }

  &__content {
    display: flex;
    align-items: start;
    margin-bottom: 145px;

    @media screen and (max-width: 1023px) {
      justify-content: center;
      margin-bottom: 49px;
    }
  }

  &__wrapper {
    margin-right: 190px;
    display: flex;
    flex-direction: column;
    padding-left: 69px;

    @media screen and (max-width: 1023px) {
      display: none;
    }
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
      background-image: url('@/images/icons/search.svg');
    }
    &_type-menu {
      background-image: url('@/images/icons/menu.svg');
      margin-top: 2px;
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
    font-family: 'Roboto', sans-serif;
    font-size: 120px;
    font-weight: 900;
    line-height: 130px;
    text-align: left;
    color: #fff;
    text-transform: uppercase;
    max-width: 627.33px;
    margin-top: 35px;
    margin-bottom: 22px;

    @media screen and (max-width: 719px) {
      font-size: 58.15px;
      line-height: 63px;
      max-width: 314px;
      margin-bottom: 9px;
    }
  }

  &__list {
    background-color: #000;
    opacity: 60%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 66.5%;
    padding: 40px 122px 38px 68px;

    @media screen and (max-width: 1360px) {
      padding-right: 40px;
      padding-left: 40px;
    }

    @media screen and (max-width: 1023px) {
      flex-direction: column;
      align-items: start;
      width: 40%;
      gap: 35px;
    }

    @media screen and (max-width: 719px) {
      width: 314px;
      padding-left: 30px;
    }

    @media screen and (max-width: 330px) {
      width: 100%;
    }
  }

  &__video {
    position: relative;
    background-image: url('@/images/hero2.png');
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    z-index: 1;
    width: 417.22px;
    aspect-ratio: 417.22/254;
    height: auto;

    @media screen and (max-width: 719px) {
      max-width: 314px;
      width: 100%;
      aspect-ratio: 314/191;
    }
  }

  &__play {
    position: absolute;
    top: 34%;
    left: 41.5%;
    background-image: url('@/images/icons/play-big.svg');
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

    @media screen and (max-width: 719px) {
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding-left: 30.5px;
      padding-right: 30.5px;
      padding-bottom: 40px;
    }
  }

  &__footer {
    display: flex;
    align-items: end;
  }

  &__social {
    transform: rotate(-90deg);
    margin-bottom: 2px;
    width: 21px;
    margin-left: 63px;
    display: flex;

    @media screen and (max-width: 1279px) {
      display: none;
    }
  }

  &__wrapper-count {
    font-family: 'DMSans', sans-serif;
    font-size: 16px;
    font-weight: 700;
    line-height: 20.83px;
    color: #fff;
    box-shadow: 0 0 4px 0 #0000001a;
    transform: rotate(-90deg);
    margin-top: 17px;
    padding-bottom: 10px;
  }
}
</style>
