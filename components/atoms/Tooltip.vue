<template>
  <v-tooltip activator="parent" location="bottom" color="purple" />
</template>
<script setup lang="ts">
</script>
<style lang="scss" scoped>
.v-tooltip.v-overlay>.v-overlay__content {
  background: rgba(var(--v-theme-surface-variant), 1);
}
</style>