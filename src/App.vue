<template>
  <input v-focus="{ firstFocus: true, color: 'green' }" type="text" />
</template>

<script setup lang="ts">
import type { Directive } from 'vue';

const vFocus: Directive<
  HTMLInputElement,
  { firstFocus: boolean; color: string }
> = {
  mounted(el, binding) {
    el.focus();
  },
};
</script>

<style lang="scss">
@import './assets/scss/base.scss';
</style>
