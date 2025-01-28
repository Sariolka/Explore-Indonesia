<script setup lang="ts">
import ButtonLearnMore from '@/components/details/ButtonRed.vue'
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
          <p class="plans__description">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus dapibus mauris in
            lectus tempus, eget tincidunt lacus varius. Sed euismod orci dictum faucibus malesuada.
            Praesent sed eros tincidunt, viverra neque auctor, lobortis enim.
          </p>
        </div>
      </li>
      <li class="plans__item">
        <div class="plans__item-header">
          <div class="plans__count-circle"><span class="plans__count">2</span></div>
          <h3 class="plans__item-title">Choosing your hotel</h3>
        </div>
        <div class="plans__container-inner">
          <div class="plans__content">
            <div class="plans__line"></div>
            <p class="plans__description">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus dapibus mauris in
              lectus tempus, eget tincidunt lacus varius. Sed euismod orci dictum faucibus
              malesuada. Praesent sed eros tincidunt, viverra neque auctor, lobortis enim.
            </p>
          </div>
          <div class="plans__item-inner">
            <img
              class="plans__img"
              src="https://images.unsplash.com/photo-1521036445206-ceb73e2de4a6?q=80&w=1976&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
              alt="plans image"
            />
            <div class="plans__container">
              <h4 class="plans__inner-title">Travelling there</h4>
              <p class="plans__inner-description">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus dapibus mauris in
                lectus tempus, eget tincidunt.
              </p>
            </div>
          </div>
        </div>
      </li>
      <li class="plans__item">
        <div class="plans__item-header">
          <div class="plans__count-circle"><span class="plans__count">3</span></div>
          <h3 class="plans__item-title">Planning your experiences</h3>
        </div>
        <div class="plans__content">
          <div class="plans__line"></div>
          <p class="plans__description">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus dapibus mauris in
            lectus tempus, eget tincidunt lacus varius.
          </p>
        </div>
      </li>
    </ul>
    <ButtonLearnMore title="Learn More" class="plans__btn" />
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

  &__list {
    padding-left: 0;
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
  }

  &__description {
    font-family: 'DMSans', sans-serif;
    font-size: 23.47px;
    font-weight: 400;
    line-height: 38.15px;
    color: rgba(21, 20, 57, 0.4);
    padding-top: 20px;
    padding-bottom: 20px;
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
    gap: 50px;
  }

  &__container-inner {
    display: flex;
    flex-direction: column;
  }

  &__img {
    width: 249.42px;
    height: 165.79px;
    object-fit: cover;
    object-position: center;
  }

  &__content {
    display: flex;
    gap: 80px;
    height: 100%;
    margin-left: 28px;
  }

  &__line {
    height: 100%;
    border: 1.45px solid rgba(21, 20, 57, 0.4);
    opacity: .3;
    display: flex;
    flex-grow: 1;
  }
}
</style>
