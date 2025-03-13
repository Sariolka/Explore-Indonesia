<script setup lang="ts">
import FooterBlock from '@/layout/FooterBlock.vue';
import PhotoGalleryBlock from '@/layout/PhotoGalleryBlock.vue';
import ArticlesBlock from '@/layout/ArticlesBlock.vue';
import ExploreBlock from '@/layout/ExploreBlock.vue';
import MapBlock from '@/layout/MapBlock.vue';
import VideoBlock from '@/layout/VideoBlock.vue';
import HeroBlock from '@/layout/HeroBlock.vue';
import PlansBlock from '@/layout/PlansBlock.vue';

const scrollUp = () => {
  if (window.pageYOffset > 0) {
    window.scrollBy(0, -75);
    setTimeout(scrollUp, 0);
  }
};
</script>

<template>
  <HeroBlock />
  <main>
    <ArticlesBlock />
    <ExploreBlock />
    <MapBlock />
    <VideoBlock />
    <PhotoGalleryBlock />
    <PlansBlock />
  </main>
  <FooterBlock @scrollUp="scrollUp" />
</template>

<style scoped></style>
