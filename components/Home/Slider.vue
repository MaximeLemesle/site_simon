<template>
  <!-- <div class="slider-container">
    <swiper :slides-per-view="3" :space-between="30" class="mySwiper">
      <swiper-slide v-for="(program, index) in programs" :key="index">
        <div class="card">
          <div class="image-placeholder">IMAGE</div>
          <div class="price">{{ program.price }} €</div>
          <div class="program-name">{{ program.name }}</div>
          <ul class="features">
            <li v-for="(feature, index) in program.features" :key="index">
              <span :class="feature.available ? 'available' : 'not-available'">
                {{ feature.available ? "✔️" : "❌" }}
              </span>
              {{ feature.name }}
            </li>
          </ul>
          <button class="discover-button">DÉCOUVRIR</button>
        </div>
      </swiper-slide>
    </swiper>
  </div> -->

  <div class="slider flex gap-x-6 items-center">
    <div class="prev">
      <img src="@/assets/icons/prev.svg" alt="Slider controller précédent" />
    </div>

    <div class="slider__content flex gap-x-8">
      <div
        class="slider__item flex flex-col gap-y-6"
        v-for="(program, index) in data.programs"
        :key="index"
      >
        <img src="@/assets/fake-image.png" alt="Fausse image" class="h-60" />

        <div class="item__content flex flex-col gap-y-4">
          <div class="item__price h3 neutre-0">{{ program.price }} €</div>
          <div class="item__name h4 primary-100">{{ program.name }}</div>
          <ul class="features flex flex-col gap-y-1.5">
            <li
              v-for="(feature, index) in program.features"
              :key="index"
              class="flex gap-x-2"
            >
              <span>
                <img
                  v-if="feature.available"
                  src="@/assets/icons/check.svg"
                  class="h-6"
                  alt="Check Icon"
                />
                <img
                  v-else
                  src="@/assets/icons/close.svg"
                  class="h-6"
                  alt="Check Icon"
                />
              </span>
              {{ feature.name }}
            </li>
          </ul>
        </div>

        <button class="btn btn-primary w-full">Découvrir</button>
      </div>
    </div>

    <div class="next">
      <img src="@/assets/icons/next.svg" alt="Slider controller suivant" />
    </div>
  </div>
</template>

<script setup>
import data from "@/data/db.json"
</script>