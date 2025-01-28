<script setup lang="ts">
import FooterBlock from '@/components/blocks/FooterBlock.vue'
import PhotoGalleryBlock from '@/components/blocks/PhotoGalleryBlock.vue'
import ArticlesBlock from '@/components/blocks/ArticlesBlock.vue'
import ExploreBlock from '@/components/blocks/ExploreBlock.vue'
import MapBlock from '@/components/blocks/MapBlock.vue'
import VideoBlock from '@/components/blocks/VideoBlock.vue'
import HeroBlock from '@/components/blocks/HeroBlock.vue'
import PlansBlock from '@/components/blocks/PlansBlock.vue'
const scrollUp = () => {
  if (window.pageYOffset > 0) {
    window.scrollBy(0, -75)
    setTimeout(scrollUp, 0)
  }
}
</script>

<template>
  <header></header>

  <main>
    <HeroBlock />
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
