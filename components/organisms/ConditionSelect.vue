<template>
  <AtomsTextField v-model="text" />
  <AtomsTextField v-model="text2" />
  <AtomsButton @click="onClick" />
</template>

<script setup lang="ts">
const text = ref('test');
const text2 = ref('test2');
const onClick = () => {
  console.log(text.value, text2.value)
}
</script>

<style lang="scss" scoped></style>
