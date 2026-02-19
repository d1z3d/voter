<script setup lang="ts">
import type { NuxtError } from "#app";

const { error } = defineProps<{
  error: NuxtError;
}>();
</script>

<template>
  <div>
    <div>{{ error.status }}</div>
    <div>{{ error.message }}</div>
  </div>
</template>
