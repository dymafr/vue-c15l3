<template>
  <input v-focus="{ firstFocus: true, color: 'green' }" type="text" />
</template>

<script setup lang="ts">
import type { Directive } from 'vue';

const vFocus: Directive<
  HTMLInputElement,
  { firstFocus: boolean; color: string }
> = {
  mounted(el, { value: { firstFocus, color } }) {
    if (firstFocus) {
      el.style.outlineColor = color;
      el.focus();
    }
  },
};
</script>

<style lang="scss">
@import './assets/scss/base.scss';
</style>
