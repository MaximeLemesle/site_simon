<template>
  <section>
    <div
      class="review__item px-36 py-14 gap-8 flex flex-col items-center"
      :class="{
        'bg-neutre-0 neutre-900': review.id % 2 !== 0,
        'bg-primary-300 neutre-0 flex-row-reverse': review.id % 2 === 0,
      }"
      v-for="review in reviews.reviews"
      v-bind:key="review.id"
    >
      <h2 class="h2">Programme de l’athlète {{ review.name }}</h2>
      <div class="review__content flex gap-12"
        :class="{
          'flex-row-reverse': review.id % 2 === 0,
        }">
        <div class="review__details flex flex-col gap-8 w-2/3">

          <h3 class="h3">Programme {{ review.program }}</h3>

          <div class="flex flex-col gap-4">
            <div class="p-2">
              <h4 class="h5">Poids de départ :</h4>
              <p>{{ review.start_weight }}kg</p>
            </div>
            <div class="p-2">
              <h4 class="h5">Poids de fin :</h4>
              <p>{{ review.final_weight }}kg</p>
            </div>
            <div class="p-2">
              <h4 class="h5">Objectif :</h4>
              <p>{{ review.objective }}</p>
            </div>
          </div>

          <div class="feedback p-2 bg-primary-500 primary-100">
            <h4 class="h5">Retour :</h4>
            <p>{{ review.feedback }}</p>
          </div>

        </div>

        <div class="review__images flex flex-col gap-3 w-1/3">
          <img
            class="h-64 w-full"
            :src="`/_nuxt/assets/reviews/${review.image_before}`"
            alt="Photo avant transformation de {{ review.name }}"
          />
          <img
            class="h-64 w-full"
            :src="`/_nuxt/assets/reviews/${review.image_after}`"
            alt="Photo après transformation de {{ review.name }}"
          />
        </div>
      </div>
    </div>
  </section>
</template>
<script setup>
import reviews from "@/data/reviews.json";
</script>