<template>
  <v-select label="Select Item" multiple>
    <slot name="selection"></slot>
  </v-select>
</template>

<script setup lang=" ts">
      </script>

<style lang="scss" scoped>
.custom-v-select .v-input__append-inner {
  display: none;
}
</style>
