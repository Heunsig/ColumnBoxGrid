<script setup lang="ts">
import { computed } from 'vue'

const props = defineProps<{
  name: string,
  description: string,
}>()

const truncatedDescription = computed(() => {
  return props.description.length > 10 
    ? props.description.slice(0, 30) + '...' 
    : props.description
})
</script>

<template>
  <div class="card">
    <h2 class="card__title">{{ name }}</h2>
    <div class="card__preview">
      {{ truncatedDescription }}
    </div>
    <div class="card__body">
      <div class="card__body-inner">
        <div class="card__description">
          <p>{{ description }}</p>
        </div>
        <div class="card__actions">
          <button 
            class="card__button"
            type="button"
          >
            <span class="card__button-text">View</span>
          </button>
        </div>
      </div>
      </div>
  </div>
</template>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  position: relative;
  background-color: #fff;
  border-radius: 0.5rem;
  border: 1px solid #e0e0e0;
  box-shadow: 0 0 3px 0 rgba(0, 0, 0, 0.1);
  padding: 0.75rem;
}

.card__title {
  margin: 0;
  font-size: 1.2rem;
  font-weight: bold;
  font-size: 1rem;
}

.card__preview {
  font-size: 0.875rem;
  color: #71717a;
  visibility: visible;
  opacity: 1;
  height: 100%;
  pointer-events: none;
}

.card__body {
  display: grid;
  grid-template-rows: 0fr;
  overflow: hidden;
  transition: grid-template-rows 0.3s ease-out;
}

.card:hover .card__preview {
  visibility: hidden;
  opacity: 0;
  height: 0px;
}

.card:hover .card__body {
  grid-template-rows: 1fr;
}

.card__body-inner {
  overflow: hidden;
}

.card__description {
  font-size: .875rem;
  color: #71717a;
  overflow: hidden;
  text-overflow: ellipsis;
}

.card__description > p {
  margin: 0;
}

.card__actions {
  margin-top: 0.75rem;
}

.card__button {
  width: 100%;
  height: 1.75rem;
  background-color: #18181b;
  color: #fff;
  border: none;
  border-radius: 0.25rem;
  cursor: pointer;
  transition: background-color 0.15s ease-in-out;
}

.card__button:hover {
  background-color: #2f2f31;
}
</style>