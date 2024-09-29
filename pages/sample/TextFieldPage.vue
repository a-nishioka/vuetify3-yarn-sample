<template>
  <h1>sample/TextFieldPage.vue</h1>
  <AtomsTextField v-model="text" label="test" @click:clear="onClear" />
  <AtomsButton @click="onClick" />
</template>
<script setup lang="ts">
const text = ref('test');

const onClear = () => {
  // focusがあたっている要素を取得
  const elem = <HTMLInputElement>document.activeElement;
  console.log("onClear", elem);
  if (elem) elem.blur();
}

const onClick = () => {
  // focusがあたっている要素を取得
  const elem = document.activeElement;
  console.log("onClick", elem);
  text.value = '';
}
</script>
<style lang="scss" scoped></style>