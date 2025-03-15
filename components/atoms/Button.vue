<template>
  <v-btn ref="btnRef" @click="onClick">Click me</v-btn>
</template>

<script setup lang="ts">
import type { VBtn } from 'vuetify/components'

const emits = defineEmits<{ (e: 'click'): void }>()
const onClick = (): void => {
  console.log('onClick')
  emits('click')
}

// v-btn の参照を作成
const btnRef = useTemplateRef<VBtn | null>('btnRef')

onMounted(() => {
  if (btnRef.value?.$el) {
    (btnRef.value.$el as HTMLButtonElement).click()
  }
})
</script>

<style lang="scss" scoped></style>
