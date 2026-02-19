<script>
const route = useRoute();
const id = ref(route.params.id);
</script>

<template>
  <div>info about post of {{ id }}</div>
</template>
