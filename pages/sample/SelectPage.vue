<template>
  <h1>sample/SelectPage.vue</h1>
  <AtomsSelect v-model="value" :items="items">
    <template #selection="{ item, index }">
      <v-chip v-if="index < 2">
        <span>{{ item.title }}</span>
      </v-chip>
      <span v-if="index === 2" class="text-grey text-caption align-self-center">
        (+{{ value.length - 2 }} others)
      </span>
    </template>
  </AtomsSelect>
</template>
<script setup lang="ts">
const items = ['foo', 'bar', 'fizz', 'buzz', 'fizzbuzz', 'foobar']

const value = ref(['foo', 'bar', 'fizz'])
</script>
<style lang="scss" scoped></style>