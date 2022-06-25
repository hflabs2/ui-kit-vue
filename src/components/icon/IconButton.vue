<template>
  <button
    class="icon-button h-vertical-middle"
    :class="{ 'no-bg-color': noBgColor }"
  >
    <Icon :icon="icon" :color="color" :size="size"></Icon>
  </button>
</template>

<script setup lang="ts">
import { defineProps } from "vue";
defineProps({
  icon: String, // the same as Icon's icon property
  color: String, // the same as Icon's color property
  size: String, // the same as Icon's size property
  noBgColor: Boolean,
});
</script>

<style scoped lang="scss">
.icon-button {
  width: 24px;
  height: 24px;
  padding: 5px;
  border: none;
  background: #fff;
  border-radius: 12px;
  margin: auto;
  box-shadow: 0 0 12px #e7e7e7;
  cursor: pointer;

  &:hover {
    opacity: 0.6;
  }

  &.no-bg-color {
    background: transparent;
    box-shadow: none;
  }
}
</style>
