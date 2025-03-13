<script setup lang="ts">
const props = defineProps<{
  title: string;
  size?: 'medium';
}>();
</script>

<template>
  <button
    class="red-button"
    :class="{ 'red-button_type-big': size === 'medium' }"
    @click="$emit('click')"
  >
    {{ title }}
  </button>
</template>

<style scoped lang="scss">
.red-button {
  border-radius: 32px;
  background-color: #dd2242;
  outline: transparent;
  color: #fff;
  font-family: 'DMSans', sans-serif;
  font-size: 18px;
  font-weight: 700;
  line-height: 27px;
  text-align: center;
  border: none;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: auto;
  cursor: pointer;

  &_type-big {
    border-radius: 211px;
    font-size: 20px;
    line-height: 30px;
    color: rgba(255, 255, 255, 0.8);
  }
}
</style>
