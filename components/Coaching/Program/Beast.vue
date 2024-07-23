<template>
  <section class="programs__details flex flex-col items-center gap-8 bg-primary-100">
    <h2 class="h2 neutre-900">{{ selectedProgram.name }}</h2>
    <div class="programs__description flex flex-col gap-3">
      <h4 class="h4">Description</h4>
      <p class="description">{{ selectedProgram.description }}</p>
    </div>
    <div class="programs__content flex gap-8">
      <div class="programs__image w-1/3">
        <img src="@/assets/beast.svg" :alt="`Image du ${selectedProgram.name}`" class="h-full w-full object-contain"/>
      </div>
      <div class="programs__features w-1/2 flex flex-col gap-y-4">
        <h4 class="h4 neutre-900">Contenu</h4>
        <ul>
          <li v-for="(feature, index) in selectedProgram.features" :key="index" class="feature-item">
            <span :class="{ 'text-green-500': feature.available, 'text-red-500': !feature.available }">
              {{ feature.available ? '✔️' : '❌' }}
            </span>
            {{ feature.name }}
            <p class="details">{{ feature.details }}</p>
          </li>
        </ul>
      </div>
    </div>
    <div class="programs__additional-info mt-8">
      <h4 class="h4 neutre-900">Informations Complémentaires</h4>
      <p>{{ selectedProgram.informations }}</p>
    </div>
    <button class="btn btn-primary mt-8">Obtenir le programme {{ selectedProgram.name }}</button>
  </section>
</template>
<script setup>
import { ref } from "vue";
import data from "@/data/programs.json";

const selectedProgram = ref(data.programs[0]);
</script>
<style scoped>
.programs__details {
  padding: 2rem;
  background-color: var(--neutre-100);
}

.programs__image img {
  max-width: 100%;
  height: auto;
}

.feature-item {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.details {
  font-size: 0.875rem;
  color: var(--neutre-700);
}

.programs__additional-info {
  margin-top: 2rem;
}

.btn-primary {
  background-color: var(--primary-500);
  color: white;
  padding: 0.5rem 1rem;
  border: none;
  border-radius: 0.25rem;
  cursor: pointer;
}

.btn-primary:hover {
  background-color: var(--primary-600);
}
</style>