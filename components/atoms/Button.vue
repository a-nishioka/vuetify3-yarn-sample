<template>
  <v-btn @click="onClick">Click me</v-btn>
</template>

<script setup lang="ts">
const emits = defineEmits<{ (e: 'click'): void }>()
const onClick = (): void => {
  emits('click')
}
</script>

<style lang="scss" scoped></style>
