<script setup lang="ts">
import ButtonLearnMore from '@/components/ButtonRed.vue'
import { ref } from 'vue'

const isTextShown1 = ref(false)
const isTextShown2 = ref(false)
const isTextShown3 = ref(false)
const isTextShown4 = ref(false)

const handleToggleText = (index: number) => {
  if (index === 1) {
    isTextShown1.value = !isTextShown1.value
  } else if (index === 2) {
    isTextShown2.value = !isTextShown2.value
  } else if (index === 3) {
    isTextShown3.value = !isTextShown3.value
  } else if (index === 4) {
    isTextShown4.value = !isTextShown4.value
  }
}
</script>

<template>
  <section class="plans">
    <h2 class="plans__title">Getting there</h2>
    <ul class="plans__list">
      <li class="plans__item">
        <div class="plans__item-header">
          <div class="plans__count-circle"><span class="plans__count">1</span></div>
          <h3 class="plans__item-title">Bookings your flights</h3>
        </div>
        <div class="plans__content">
          <div class="plans__line"></div>
          <p
            class="plans__description-text"
            :class="{ 'plans__description-text_hide': !isTextShown1 }"
          >
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus dapibus mauris in
            lectus tempus, eget tincidunt lacus varius. Sed euismod orci dictum faucibus malesuada.
            Praesent sed eros tincidunt, viverra neque auctor, lobortis enim.
          </p>
        </div>
        <button class="plans__text-show-more" @click="handleToggleText(1)">
          {{ isTextShown1 ? 'Show less' : 'Show more' }}
        </button>
      </li>
      <li class="plans__item">
        <div class="plans__item-header">
          <div class="plans__count-circle"><span class="plans__count">2</span></div>
          <h3 class="plans__item-title">Choosing your hotel</h3>
        </div>
        <div class="plans__container-inner">
          <div class="plans__content">
            <div class="plans__line"></div>
            <div class="plans__description">
              <p
                class="plans__description-text"
                :class="{ 'plans__description-text_hide': !isTextShown4 }"
              >
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus dapibus mauris in
                lectus tempus, eget tincidunt lacus varius. Sed euismod orci dictum faucibus
                malesuada. Praesent sed eros tincidunt, viverra neque auctor, lobortis enim.
              </p>
              <button class="plans__text-show-more" @click="handleToggleText(4)">
                {{ isTextShown4 ? 'Show less' : 'Show more' }}
              </button>
              <div class="plans__item-inner">
                <div class="plans__img-container">
                  <img
                    class="plans__img"
                    src="https://images.unsplash.com/photo-1521036445206-ceb73e2de4a6?q=80&w=1976&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                    alt="plans image"
                  />
                  <button class="plans__img-btn"></button>
                </div>

                <div class="plans__container">
                  <h4 class="plans__item-title plans__item-title_type-inner">Travelling there</h4>
                  <p
                    class="plans__description-text plans__description-text_type-inner"
                    :class="{ 'plans__description-text_hide': !isTextShown2 }"
                  >
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus dapibus
                    mauris in lectus tempus, eget tincidunt.
                  </p>
                </div>
                <button class="plans__text-show-more" @click="handleToggleText(2)">
                  {{ isTextShown2 ? 'Show less' : 'Show more' }}
                </button>
              </div>
            </div>
          </div>
        </div>
      </li>
      <li class="plans__item">
        <div class="plans__item-header">
          <div class="plans__count-circle"><span class="plans__count">3</span></div>
          <h3 class="plans__item-title">Planning your experiences</h3>
        </div>
        <div class="plans__content plans__content_type-last">
          <p
            class="plans__description-text plans__description-text_type-last"
            :class="{ 'plans__description-text_hide': !isTextShown3 }"
          >
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus dapibus mauris in
            lectus tempus, eget tincidunt lacus varius.
          </p>
        </div>
        <button class="plans__text-show-more" @click="handleToggleText(3)">
          {{ isTextShown3 ? 'Show less' : 'Show more' }}
        </button>
      </li>
    </ul>
    <ButtonLearnMore title="Learn More" class="plans__btn" />
  </section>
</template>

<style scoped lang="scss">
.plans {
  display: flex;
  flex-direction: column;
  padding: 114px 386px 120px;
  background-color: #dce8f2;

  @media screen and (max-width: 1450px) {
    padding-left: 150px;
    padding-right: 150px;
  }

  @media screen and (max-width: 1023px) {
    padding-left: 50px;
    padding-right: 50px;
  }

  @media screen and (max-width: 719px) {
    padding: 33px 30.5px 80px;
  }

  &__title {
    font-family: 'DMSans', sans-serif;
    font-size: 60px;
    font-weight: 700;
    line-height: 90px;
    color: #010a20;
    margin-bottom: 35px;

    @media screen and (max-width: 719px) {
      font-size: 40px;
      line-height: 46px;
      margin-right: auto;
      margin-left: auto;
      margin-bottom: 40px;
    }
  }

  &__list {
    padding-left: 0;
    @media screen and (max-width: 719px) {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      width: 100%;
      gap: 30px;
    }
  }

  &__item {
    display: flex;
    flex-direction: column;
  }

  &__item-title {
    font-family: 'DMSans', sans-serif;
    font-size: 26.41px;
    font-weight: 700;
    line-height: 41.08px;
    color: #010a20;
    margin-top: 5px;

    &_type-inner {
      margin-top: 1px;

      @media screen and (max-width: 719px) {
        display: none;
      }
    }

    @media screen and (max-width: 719px) {
      font-size: 22px;
      line-height: 33px;
    }
  }

  &__text-show-more {
    display: none;
    border: none;
    background-color: transparent;

    @media screen and (max-width: 719px) {
      display: flex;
      justify-content: center;
      font-size: 16px;
      line-height: 24px;
      letter-spacing: 0.5px;
      font-family: 'DMSans', sans-serif;
      font-weight: 400;
      color: #dd2242;
    }
  }

  &__description {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  &__item-inner {
    display: flex;
    align-items: start;
    margin-top: 12px;
    gap: 45px;
    margin-bottom: 9px;

    @media screen and (max-width: 1366px) {
      flex-direction: column;
      align-items: center;
      gap: 0;
    }

    @media screen and (max-width: 719px) {
      margin-top: 35px;
      gap: 0;
    }
  }

  &__description-text {
    font-family: 'DMSans', sans-serif;
    font-size: 23.47px;
    font-weight: 400;
    line-height: 38.15px;
    color: rgba(21, 20, 57, 0.4);
    padding-top: 22px;
    padding-bottom: 85px;

    @media screen and (max-width: 719px) {
      font-size: 16px;
      line-height: 24px;
      letter-spacing: 0.5px;
      padding-bottom: 0;
      padding-top: 5px;
      max-width: 200px;
    }

    &_hide {
      @media screen and (max-width: 719px) {
        overflow: hidden;
        display: -webkit-box;
        -webkit-line-clamp: 1;
        line-clamp: 1;
        -webkit-box-orient: vertical;
        text-overflow: ellipsis;
        max-width: 200px;
      }
    }

    &_type-inner {
      padding-top: 12px;
      max-width: 450px;

      @media screen and (max-width: 719px) {
        max-width: 220px;
      }
    }

    &_type-last {
      padding-bottom: 20px;
      @media screen and (max-width: 719px) {
        padding-bottom: 0;
      }
    }
  }
  &__container {
    display: flex;
    flex-direction: column;
    width: 100%;
    align-items: center;
  }

  &__count-circle {
    width: 58.64px;
    height: 58.64px;
    border-radius: 50%;
    background-color: #dd2242;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  &__count {
    font-family: 'DMSans', sans-serif;
    font-size: 26.41px;
    font-weight: 500;
    line-height: 38.15px;
    color: #fff;
    position: absolute;
  }

  &__item-header {
    display: flex;
    align-items: center;
    gap: 44px;

    @media screen and (max-width: 719px) {
      flex-direction: column;
      gap: 16px;
    }
  }

  &__container-inner {
    display: flex;
    flex-direction: column;
  }

  &__img {
    width: 249.42px;
    height: 165.79px;
    aspect-ratio: 249.42/165.79;
    object-fit: cover;
    object-position: center 70%;
    border-radius: 7.34px;
    margin-bottom: 45px;

    @media screen and (max-width: 719px) {
      width: 100%;
      height: auto;
      aspect-ratio: 249.42/165.79;
      margin-bottom: 20px;
    }
  }

  &__img-container {
    position: relative;
  }

  &__img-btn {
    position: absolute;
    top: 80px;
    left: 50%;
    background-image: url('@/images/icons/play.svg');
    width: 16px;
    height: 18px;
    background-color: transparent;
    border: none;
    cursor: pointer;

    @media screen and (max-width: 1279px) {
      top: 95px;
      left: 48%;
    }
  }

  &__content {
    display: flex;
    align-items: stretch;
    gap: 71px;
    height: 100%;
    margin-left: 30px;

    &_type-last {
      padding-left: 71px;
    }

    @media screen and (max-width: 719px) {
      margin-left: 0;
    }
  }

  &__line {
    height: auto;
    border-left: 2.93px solid rgba(21, 20, 57, 0.4);
    opacity: 0.3;
    display: flex;
    flex-grow: 1;

    @media screen and (max-width: 719px) {
      display: none;
    }
  }

  &__btn {
    width: 210px;
    height: 64px;
    margin-left: 101px;
    @media screen and (max-width: 719px) {
      display: none;
    }
  }
}
</style>
