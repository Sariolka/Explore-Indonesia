<script setup lang="ts">
import ByTheNumbersBlock from '@/components/blocks/ByTheNumbersBlock.vue'
</script>

<template>
  <section class="explore">
    <ByTheNumbersBlock />
  </section>
</template>

<style scoped lang="scss">
.explore {
  background-image: url('../images/explore.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  height: 2207px;
  background-position: center;
  display: flex;
  flex-direction: column;
  justify-content: end;
}
</style>
