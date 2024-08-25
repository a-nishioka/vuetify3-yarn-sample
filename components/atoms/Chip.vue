<template>
  <v-chip :text="text" :variant="variant" density="default" size="default">
  </v-chip>
</template>

<script setup lang="ts">
defineProps
  ({
    text: { type: String, default: 'text' },
    variant: { type: String, default: 'tonal' },
  });

</script>

<style lang="scss" scoped></style>
