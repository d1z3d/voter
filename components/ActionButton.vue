<script setup lang="ts">
interface Props {
  width?: number | string;
  height?: number | string;
}

const props = withDefaults(defineProps<Props>(), {
  width: 301,
  height: 41,
});

const buttonStyle = computed(() => ({
  width: normalizeDimension(props.width),
  height: normalizeDimension(props.height),
}));

function normalizeDimension(value: number | string): string {
  return typeof value === "number" ? `${value}px` : value;
}
</script>

<template>
  <button class="button" :style="buttonStyle">
    <slot />
  </button>
</template>

<style scoped>
.button {
  border-radius: 20px;
  background-color: #191919;
}
</style>
