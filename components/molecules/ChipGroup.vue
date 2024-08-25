<template>
  <v-chip-group column>
    <AtomsChip v-for="item in items" :key="item" :text="item" />
  </v-chip-group>
</template>

<script setup lang="ts">
defineProps({
  items: { type: Array<string>, default: [] },
});
</script>

<style lang="scss" scoped></style>
