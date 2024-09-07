<template>
  <div id="slider" class="flex gap-6 items-center w-full">
    <!-- Previous Slide Button -->
    <div
      class="control prev py-8 px-4"
      @click="prevSlide"
      :style="controlStyle"
    >
      <img
        :src="
          isFirstSlide
            ? '/_nuxt/assets/icons/prev-disabled.svg'
            : '/_nuxt/assets/icons/prev.svg'
        "
        alt="Slider controller précédent"
      />
    </div>

    <!-- Slider Content -->
    <div class="slider__content flex overflow-hidden relative w-full">
      <div class="slider-wrapper flex gap-8" :style="wrapperStyle">
        <div
          class="slider__item flex flex-col gap-6"
          v-for="(program, index) in data.programs"
          :key="index"
          :style="itemStyle"
        >
          <img src="@/assets/fake-image.png" alt="Fausse image" class="h-60" />
          <div class="item__content flex flex-col gap-4">
            <div class="item__price h3 neutre-0">{{ program.price }} €</div>
            <div class="item__name h4 primary-100">{{ program.name }}</div>
            <ul class="features flex flex-col gap-1.5">
              <li
                v-for="(feature, index) in program.features"
                :key="index"
                class="flex gap-2"
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
                    alt="Close Icon"
                  />
                </span>
                {{ feature.name }}
              </li>
            </ul>
          </div>
          <button class="btn btn-primary !w-full">Découvrir</button>
        </div>
      </div>
    </div>

    <!-- Next Slide Button -->
    <div
      class="control next py-8 px-4"
      @click="nextSlide"
      :style="controlStyle"
    >
      <img
        :src="
          isLastSlide
            ? '/_nuxt/assets/icons/next-disabled.svg'
            : '/_nuxt/assets/icons/next.svg'
        "
        alt="Slider controller suivant"
      />
    </div>
  </div>
</template>
<script setup>
import { ref, computed, onMounted, onUnmounted } from "vue";
import data from "@/data/programs.json";

const startIndex = ref(0);
const itemsToShow = ref(3);

const updateItemsToShow = () => {
  const width = window.innerWidth;
  if (width <= 640) {
    itemsToShow.value = 1;
  } else if (width <= 1024) {
    itemsToShow.value = 2;
  } else {
    itemsToShow.value = 3;
  }
};

onMounted(() => {
  updateItemsToShow();
  window.addEventListener("resize", updateItemsToShow);
});

onUnmounted(() => {
  window.removeEventListener("resize", updateItemsToShow);
});

const itemGap = 16;
const itemWidth = computed(() => 100 / itemsToShow.value);

const wrapperStyle = computed(() => {
  const translateX = startIndex.value * (itemWidth.value + itemGap);
  return {
    transform: `translateX(-${translateX}%)`,
    transition: "transform 0.5s ease-in-out",
    gap: `${itemGap}px`,
  };
});

const itemStyle = computed(() => ({
  width: `${itemWidth.value}%`,
}));

const isFirstSlide = computed(() => startIndex.value === 0);
const isLastSlide = computed(
  () => startIndex.value >= data.programs.length - itemsToShow.value
);

const prevSlide = () => {
  if (startIndex.value > 0) {
    startIndex.value -= 1;
  }
};

const nextSlide = () => {
  if (startIndex.value < data.programs.length - itemsToShow.value) {
    startIndex.value += 1;
  }
};
</script>
<style scoped>
.control:hover {
  cursor: pointer;
}

.slider-wrapper {
  transition: transform 0.5s ease-in-out;
}

.slider__item {
  transition: transform 0.3s ease;
}

.control img {
  width: 40px;
  height: 40px;
}
</style>