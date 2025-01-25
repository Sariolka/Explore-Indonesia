<script setup lang="ts">
import FooterBlock from '@/components/blocks/FooterBlock.vue'
import PlansBlock from '@/components/blocks/PlansBlock.vue'
import PhotoGalleryBlock from '@/components/blocks/PhotoGalleryBlock.vue'
import ArticlesBlock from '@/components/blocks/ArticlesBlock.vue'
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
    <ArticlesBlock />
    <PhotoGalleryBlock />
    <!--    <PlansBlock />-->
  </main>
  <FooterBlock @scrollUp="scrollUp" />
</template>

<style scoped></style>
