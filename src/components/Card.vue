<script setup lang="ts">
defineProps<{
  name: string,
  description: string,
}>()
</script>

<template>
  <div class="card">
    <h2>{{ name }}</h2>
    <p>{{ description }}</p>
  </div>
</template>

<style scoped>
.card {
  height: 60px;
  transition: height 0.3s ease-in-out;
}

.card:hover {
  height: 120px;
}
</style>