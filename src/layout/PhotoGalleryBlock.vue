<script setup lang="ts"></script>

<template>
  <section class="gallery">
    <h2 class="gallery__title">Photo Gallery</h2>
    <p class="gallery__description">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus dapibus mauris in lectus
      tempus, eget tincidunt.
    </p>
    <div class="gallery__images">
      <img
        src="https://images.unsplash.com/photo-1469967700385-5b0140e16e33?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        alt="gallery"
        class="gallery__image gallery__image_type-1"
      />
      <img
        src="https://images.unsplash.com/photo-1524341661047-3a38ae8987f9?q=80&w=1974&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        alt="gallery"
        class="gallery__image gallery__image_type-2"
      />
      <img
        src="https://images.unsplash.com/photo-1512631118612-7bf02594062b?q=80&w=1964&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        alt="gallery"
        class="gallery__image gallery__image_type-3"
      />
      <img
        src="https://images.unsplash.com/photo-1476158085676-e67f57ed9ed7?q=80&w=2072&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        alt="gallery"
        class="gallery__image gallery__image_type-4"
      />
      <img
        src="https://images.unsplash.com/photo-1523592121529-f6dde35f079e?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        alt="gallery"
        class="gallery__image gallery__image_type-5"
      />
      <img
        src="https://images.unsplash.com/photo-1514351606796-9d81063e482d?q=80&w=1718&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        alt="gallery"
        class="gallery__image gallery__image_type-6"
      />
    </div>
  </section>
</template>

<style scoped lang="scss">
.gallery {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 100px;
  cursor: default;

  @media screen and (max-width: 1024px) {
    padding-right: 50px;
    padding-left: 50px;
  }

  @media screen and (max-width: 1023px) {
    padding-left: 30.5px;
    padding-right: 30.5px;
  }

  &__title {
    font-family: 'DMSans', sans-serif;
    font-size: 60px;
    font-weight: 700;
    line-height: 90px;
    text-align: center;

    margin-bottom: 22px;
    letter-spacing: -0.01em;
    color: #010a20;

    @media screen and (max-width: 719px) {
      font-size: 40px;
      line-height: 46px;
    }
  }

  &__description {
    font-family: 'DMSans', sans-serif;
    text-align: center;
    color: #6f7787;
    font-size: 18px;
    font-weight: 400;
    line-height: 28px;
    letter-spacing: 0.011em;
    margin-bottom: 62px;
    max-width: 511px;

    @media screen and (max-width: 719px) {
      font-size: 16px;
      line-height: 24px;
    }
  }

  &__images {
    display: grid;
    grid-template-areas:
      'a b c'
      'a e c'
      'a e f'
      'd e f';
    grid-template-columns: repeat(3, minmax(1fr, 370px));
    grid-auto-rows: auto;
    gap: 30px;

    @media screen and (max-width: 1024px) {
      gap: 10px;
    }

    @media screen and (max-width: 719px) {
      grid-template-columns: repeat(2, minmax(1fr, 370px));
      grid-template-areas:
        'a b'
        'a e'
        'd e'
        'c f'
        'c f';
    }
  }

  &__image {
    object-fit: cover;
    object-position: center;
    width: 100%;
    border-radius: 10px;
  }

  &__image_type-1 {
    grid-area: d;
    aspect-ratio: 37/21;
  }

  &__image_type-2 {
    grid-area: a;
    aspect-ratio: 37/53;
  }

  &__image_type-3 {
    grid-area: c;
    aspect-ratio: 1/1;
  }

  &__image_type-4 {
    grid-area: e;
    aspect-ratio: 37/53;
  }

  &__image_type-5 {
    grid-area: b;
    aspect-ratio: 37/21;
  }

  &__image_type-6 {
    grid-area: f;
    aspect-ratio: 1/1;
  }
}
</style>
