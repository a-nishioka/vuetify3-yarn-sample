<template>
  <h1>sample/ChipGroupPage</h1>
  <MoleculesChipGroup :items="items"></MoleculesChipGroup>
</template>

<script setup lang="ts">
const items = [
  'Work',
  'Home Improvement',
  'Vacation',
  'Food',
  'Drawers',
  'Shopping',
  'Art',
  'Tech',
  'Creative Writing',
]
</script>

<style lang="scss" scoped></style>
