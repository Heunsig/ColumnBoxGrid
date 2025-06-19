<script setup lang="ts" generic="T extends { id: number }">
import { computed } from 'vue';

const props = withDefaults(defineProps<{
  items: T[];
  columnsCount?: number;
}>(), {
  columnsCount: 3,
  items: () => [],
})

const totalItems = computed(() => props.items.length);

const columns = computed(() => {
  const cols: Array<T[]> = Array.from({ length: props.columnsCount }, () => []);

  for (let i = 0 ; i < totalItems.value ; i++) {
    cols[i % props.columnsCount].push(props.items[i]);
  }

  return cols;
})

</script>

<template>
  <div class="box-container">
    <div 
      class="box-container__column" 
      v-for="(column, i) in columns" 
      :key="i"
    >
      <slot v-for="item in column" :item="item" :key="item.id" />
    </div>
  </div>
</template>

<style scoped>
.box-container {
  display: flex;
  gap: 1rem;

  .box-container__column {
    flex: 1 1 0;
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }
}
</style>