<template>
  <h1>index.vue</h1>
  <v-container class="container d-flex align-center justify-center" fluid>
    <v-card width="800px">
      <template v-slot:title>
        <span class="font-weight-black">Welcome to Vuetify</span>
      </template>

      <v-card-text class="pt-4 d-flex flex-columns justify-space-between ga-4">
        <div class="w-50">
          テキスト
        </div>
        <div class="w-50">
          <div>テキスト</div>
          <AtomsTextField></AtomsTextField>
          <div>テキスト</div>
          <AtomsTextField></AtomsTextField>
          <div>テキスト</div>
          <MoleculesChipGroup :items="items"></MoleculesChipGroup>
          <div>テキスト</div>
          <MoleculesChipGroup :items="items"></MoleculesChipGroup>
        </div>
      </v-card-text>
    </v-card>
  </v-container>
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
<style>
.container {
  height: 96vh;
}
</style>