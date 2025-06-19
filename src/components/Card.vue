<script setup lang="ts">
defineProps<{
  name: string,
  description: string,
}>()
</script>

<template>
  <div class="card">
    <h2 class="card__title">{{ name }}</h2>
    <div 
      class="card__body"
      :class="{ 'card__body--no-description': !description }"
    >
      <div class="card__body-inner">
        <div 
          v-if="description"
          class="card__description"
        >
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
  background-color: #fff;
  border-radius: 0.5rem;
  border: 1px solid #e0e0e0;
  box-shadow: 0 0 3px 0 rgba(0, 0, 0, 0.1);
  padding: 0.75rem;
}

.card__title {
  margin: 0;
  font-size: 1rem;
  font-weight: bold;
}
.card__body {
  margin-top: 0.5rem;
  display: grid;
  grid-template-rows: minmax(1.5rem, 0fr);
  transition: grid-template-rows 0.3s ease;
}

.card__body--no-description {
  margin-top: 0;
  grid-template-rows: minmax(0rem, 0fr);
}

.card:hover .card__body {
  grid-template-rows: minmax(1.5rem, 1fr);
}

.card__body-inner {
  overflow: hidden;
}

.card__description {
  min-height: 1.5rem;
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