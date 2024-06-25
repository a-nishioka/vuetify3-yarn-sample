<template>
  <v-select v-model="selected" :items="items" label="Select an item"
    :menu-icon="isOpen ? 'mdi-chevron-up' : 'mdi-chevron-down'" @click:menu="toggleMenu">
    <template v-slot:append-inner>
      <!-- 空のスロットを追加することでデフォルトのアイコンを隠す -->
    </template>
  </v-select>
</template>

<script setup lang="ts">
const selected = ref<string | null>(null);
const items = ref<string[]>(['Item 1', 'Item 2', 'Item 3']);
const isOpen = ref(false);
const toggleMenu = () => {
  isOpen.value = !isOpen.value;
};
</script>

<style lang="scss" scoped>
.custom-v-select .v-input__append-inner {
  display: none;
}
</style>
