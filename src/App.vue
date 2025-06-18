<script setup lang="ts">
import { computed } from 'vue';
import BoxContainer from './components/BoxContainer.vue';
import Card from './components/Card.vue';

const items = computed(() => {
  return [
    {
      id: 1,
      name: 'Item 1',
      description: 'Description 1',
    },
    {
      id: 2,
      name: 'Item 2',
      description: 'Description 2',
    },
    {
      id: 3,
      name: 'Item 3',
      description: 'Description 3',
    },
    {
      id: 4,
      name: 'Item 4',
      description: 'Description 4',
    },
    {
      id: 5,
      name: 'Item 5',
      description: 'Description 5',
    },
    {
      id: 6,
      name: 'Item 6',
      description: 'Description 6',
    },
    {
      id: 7,
      name: 'Item 7',
      description: 'Description 7',
    },
  ]
})

</script>

<template>
  <div>
    <h1>Hello World</h1>
    <BoxContainer 
      :items="items"
    >
      <template #default="{ item }">
        <Card :name="item.name" :description="item.description" />
      </template>
    </BoxContainer>
  </div>
</template>