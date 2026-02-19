<script setup lang="ts">
const route = useRoute();
const id = ref(route.params.id);
</script>

<template>
  <div>Post of {{ id }}</div>
</template>
