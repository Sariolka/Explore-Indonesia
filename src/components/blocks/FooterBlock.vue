<script setup lang="ts">
import facebook from '@/components/icons/facebook.png'
import google from '@/components/icons/google.png'
import linkedin from '@/components/icons/linkedin.png'
import logo from '@/components/images/logo-footer.svg'
import up from '@/components/icons/union.svg'
const computerYear = new Date().getFullYear()
</script>

<template>
  <footer class="footer">
    <div class="footer__nav-container">
      <img class="footer__logo" alt="logo" :src="logo" />
      <nav class="footer__nav">
        <a href="#" class="footer__link">About</a>
        <a href="#" class="footer__link">Pricing</a>
        <a href="#" class="footer__link">Company</a>
        <a href="#" class="footer__link">Blog</a>
      </nav>
    </div>
    <div class="footer__social-container">
      <div class="footer__links">
        <a href="#"><img :src="facebook" alt="facebook" class="footer__icon" /></a>
        <a href="#"><img :src="linkedin" alt="linkedin" class="footer__icon" /></a>
        <a href="#"><img :src="google" alt="google" class="footer__icon" /></a>
      </div>
      <div class="footer__copyright">
        <button class="footer__up" aria-label="up" @click="$emit('scroll-up')">
          <img class="footer__img-up" :src="up" alt="up" /></button
        >Copyright © {{ computerYear }}
      </div>
    </div>
  </footer>
</template>

<style scoped lang="scss">
.footer {
  background-color: #010a20;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 40px 149px 30px 70px;
  position: relative;
  @media screen and (max-width: 1279px) {
    padding-right: 20px;
    padding-left: 20px;
  }

  @media screen and (max-width: 1023px) {
    flex-direction: column;
  }

  @media screen and (max-width: 719px) {
    padding-bottom: 85px;
    padding-top: 145px;
  }

  &__nav-container {
    display: flex;
    align-items: center;
    gap: 123px;

    @media screen and (max-width: 1279px) {
      gap: 20px;
    }

    @media screen and (max-width: 1023px) {
      width: 100%;
      justify-content: space-between;
    }

    @media screen and (max-width: 719px) {
      flex-direction: column;
    }
  }

  &__social-container {
    display: flex;
    align-items: center;
    gap: 50px;

    @media screen and (max-width: 1023px) {
      width: 100%;
      justify-content: end;
    }

    @media screen and (max-width: 719px) {
      flex-direction: column;
      gap: 30px;
    }
  }

  &__logo {
    width: 174px;
    height: 65.75px;
    object-fit: contain;
    object-position: center;
  }

  &__nav {
    display: flex;
    align-items: center;
    gap: 35.5px;

    @media screen and (max-width: 719px) {
      flex-direction: column;
      margin-top: 19px;
    }
  }

  &__links {
    display: flex;
    align-items: center;
    gap: 21px;
    margin-top: 2px;

    @media screen and (max-width: 719px) {
      margin-top: 35px;
      gap: 48px;
    }
  }

  &__link {
    text-decoration: none;
    font-family: 'DMSans', sans-serif;
    font-size: 18px;
    font-weight: 700;
    line-height: 28px;
    letter-spacing: 0.5px;
    color: #fff;

    @media screen and (max-width: 719px) {
      font-size: 22.94px;
      line-height: 35.69px;
      letter-spacing: 0.6373105049133301px;
    }
  }

  &__icon {
    width: 24px;
    height: 24px;
    object-fit: contain;
    object-position: center;

    @media screen and (max-width: 719px) {
      width: 31px;
      height: 31px;
    }
  }

  &__copyright {
    font-family: 'DMSans', sans-serif;
    font-size: 18px;
    font-weight: 700;
    line-height: 28px;
    letter-spacing: 0.5px;
    color: #fff;
    white-space: nowrap;

    @media screen and (max-width: 719px) {
      font-size: 23.24px;
      line-height: 36.15px;
      letter-spacing: 0.6455696225166321px;
      position: relative;
    }
  }

  &__up {
    background-color: #dd2242;
    border: none;
    outline: transparent;
    position: absolute;
    right: 95px;
    bottom: 85px;
    cursor: pointer;
    width: 104px;
    height: 104px;
    box-shadow: 0 7px 10px 0 #00000033;
    border-radius: 50%;
    @media screen and (max-width: 1023px) {
      bottom: 115px;
    }
    @media screen and (max-width: 719px) {
      right: 55px;
      bottom: 575px;
    }
  }

  &__img-up {
    object-position: center;
    object-fit: contain;
  }
}
</style>
