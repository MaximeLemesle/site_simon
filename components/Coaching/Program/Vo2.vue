<template>
  <section
    class="programs__details flex flex-col items-center gap-8 bg-primary-300 neutre-0"
  >
    <h2 class="h2">{{ selectedProgram.name }}</h2>
    <div class="programs__description flex flex-col gap-3 w-full">
      <h4 class="h4">Description</h4>
      <p class="description">{{ selectedProgram.description }}</p>
    </div>
    <div class="programs__content flex flex-row-reverse gap-8">
      <div class="programs__image w-2/5">
        <img
          src="@/assets/beast.svg"
          :alt="`Image du ${selectedProgram.name}`"
          class="h-full w-full object-contain"
        />
      </div>
      <div class="programs__features w-3/5 flex flex-col gap-4">
        <h4 class="h4">Contenu</h4>
        <ul class="flex flex-col gap-4">
          <li
            v-for="(feature, index) in selectedProgram.features"
            :key="index"
            class="feature__item flex flex-col gap-1.5"
          >
            <div class="feature__title flex gap-2">
              <span>
                {{ feature.available ? "✔️" : "❌" }}
              </span>
              <p class="feature__name primary-700 font-bold">
                {{ feature.name }}
              </p>
            </div>
            <p class="feature__details">{{ feature.details }}</p>
          </li>
        </ul>
      </div>
    </div>
    <div class="programs__information flex flex-col gap-3">
      <h4 class="h4">Informations Complémentaires</h4>
      <p>{{ selectedProgram.informations }}</p>
    </div>
    <button class="btn btn-primary">
      Obtenir le programme {{ selectedProgram.name }}
    </button>
  </section>
</template>
<script setup>
import { ref } from "vue";
import data from "@/data/programs.json";

const selectedProgram = ref(data.programs[1]);
</script>
<style scoped></style>