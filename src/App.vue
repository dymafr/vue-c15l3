<template>
  <input v-focus type="text" />
</template>

<script setup lang="ts">
import type { Directive } from 'vue';

const vFocus: Directive<HTMLInputElement, boolean> = {
  mounted(el, binding) {
    el.focus();
  },
};
</script>

<style lang="scss">
@import './assets/scss/base.scss';
</style>
