<script setup lang="ts">
import VideoCard from '@/components/VideoCard.vue';
</script>

<template>
  <section class="video">
    <img
      class="video__background"
      alt="background"
      src="https://images.unsplash.com/photo-1449480881392-716d0ea24a47?q=80&w=1932&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
    />
    <h2 class="video__title">
      Live a life like you wouldn’t imagine, experience a life you wouldn’t expect.
    </h2>
    <div class="video__img-container">
      <img
        class="video__img"
        alt="video"
        src="https://images.unsplash.com/photo-1527965408463-82ae0731825c?q=80&w=2071&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
      />
      <button class="video__btn" aria-label="play"></button>
    </div>

    <div class="video__cards">
      <VideoCard
        title="In The Country"
        image="https://images.unsplash.com/photo-1449480881392-716d0ea24a47?q=80&w=1932&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus dapibus mauris in lectus tempus."
      />
      <VideoCard
        title="In The City"
        image="https://images.unsplash.com/photo-1555043722-4523972f07ee?q=80&w=1974&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus dapibus mauris in."
      />
    </div>
  </section>
</template>

<style scoped lang="scss">
.video {
  width: 100%;
  padding: 145px 200px 250px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  position: relative;
  background-color: #010a20;
  z-index: -1;

  @media screen and (max-width: 719px) {
    padding: 85px 30px;
  }

  &__title {
    font-family: 'DMSans', sans-serif;
    font-size: 42px;
    font-weight: 700;
    line-height: 50px;
    color: #ffffff;
    text-align: center;
    max-width: 1056px;
    margin-bottom: 110px;

    @media screen and (max-width: 719px) {
      font-size: 40px;
      line-height: 46px;
      margin-bottom: 67px;
    }
  }

  &__img-container {
    position: relative;
  }

  &__btn {
    position: absolute;
    top: 41.4%;
    left: 45.5%;
    background-image: url('@/images/icons/play.svg');
    background-repeat: no-repeat;
    background-position: center;
    width: 16px;
    height: 18px;
    border: none;
    cursor: pointer;
    padding: 48px;
    border-radius: 50%;
    background-color: #dd2242;

    @media screen and (max-width: 1023px) {
      padding: 33.5px;
      top: 40%;
      left: 44%;
    }

    @media screen and (max-width: 819px) {
      top: 32%;
      left: 42%;
    }
  }

  &__img {
    max-width: 1056px;
    width: 100%;
    border-radius: 10px;
    aspect-ratio: 1056/594;
    object-fit: cover;

    @media screen and (max-width: 719px) {
      aspect-ratio: 314/192;
    }
  }

  &__background {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -1;
    object-fit: cover;
    object-position: center;
    opacity: 46%;
  }

  &__cards {
    margin-top: 118px;
    display: flex;
    align-items: start;
    position: relative;
    z-index: 2;
    gap: 130px;

    @media screen and (max-width: 1023px) {
      gap: 33px;
    }

    @media screen and (max-width: 719px) {
      flex-direction: column;
      margin-top: 35px;
    }
  }
}
</style>
