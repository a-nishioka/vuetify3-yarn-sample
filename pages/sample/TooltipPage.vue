<template>
  <h1>sample/TooltipPage.vue</h1>
  <p ref="textElement" class="ellipsis">{{ message }}
    <AtomsTooltip v-if="isOverflowing" :text="message" />
  </p>
</template>
<script setup lang="ts">
const textElement = ref<HTMLElement | null>(null);
const isOverflowing = ref(false);
const message = "このテキストを省略したい。このテキストを省略したい。このテキストを省略したい。"


const checkOverflow = () => {
  if (textElement.value) {
    isOverflowing.value = textElement.value.scrollWidth > textElement.value.clientWidth;
  }
};

onMounted(() => {
  checkOverflow();
  window.addEventListener('resize', checkOverflow);
});

onBeforeUnmount(() => {
  window.removeEventListener('resize', checkOverflow);
});

watch(textElement, () => {
  checkOverflow();
});
</script>

<style lang="scss" scoped>
.ellipsis {
  width: 300px;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}
</style>