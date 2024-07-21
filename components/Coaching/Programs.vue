<template>
  <section
    class="programs px-36 py-14 flex flex-col items-center gap-y-8 bg-neutre-0"
  >
    <h2 class="h2 neutre-900">Les différents programmes hybrides</h2>
    <div class="programs__content flex items-center gap-6">
      <div
        class="programs__miniature miniature__beast h-44 w-44 cursor-pointer"
        @click="displayBeast"
        :class="{ selected: showBeastProgram }"
      ></div>
      <div
        class="programs__miniature miniature__vo2 h-44 w-44 cursor-pointer"
        @click="displayVo2"
        :class="{ selected: showVo2Program }"
      ></div>
      <div
        class="programs__miniature miniature__puissance h-44 w-44 cursor-pointer"
        @click="displayPuissance"
        :class="{ selected: showPuissanceProgram }"
      ></div>
    </div>
    <div v-if="showBeastProgram" class="programs__details">
      <h3 class="h3 neutre-900">Beast</h3>
    </div>
    <div v-if="showVo2Program" class="programs__details">
      <h3 class="h3 neutre-900">Vo2</h3>
    </div>
    <div v-if="showPuissanceProgram" class="programs__details">
      <h3 class="h3 neutre-900">Puissance</h3>
    </div>
  </section>
</template>
<script setup>
import { ref } from "vue";
// import data from "@/data/programs.json";

const showBeastProgram = ref(true);
const showVo2Program = ref(false);
const showPuissanceProgram = ref(false);

const displayBeast = () => {
  showBeastProgram.value = true;
  showVo2Program.value = false;
  showPuissanceProgram.value = false;
};

const displayVo2 = () => {
  showBeastProgram.value = false;
  showVo2Program.value = true;
  showPuissanceProgram.value = false;
};

const displayPuissance = () => {
  showBeastProgram.value = false;
  showVo2Program.value = false;
  showPuissanceProgram.value = true;
};
</script>
<style scoped>
.programs__miniature {
  background-size: contain;
  background-position: center;
  background-repeat: no-repeat;
}

.miniature__beast {
  background-image: url("@/assets/fake-mini-beast.png");
}

.miniature__vo2 {
  background-image: url("@/assets/fake-mini-vo2.png");
}

.miniature__puissance {
  background-image: url("@/assets/fake-mini-puissance.png");
}

.programs__miniature.selected {
  border: 5px solid #9cacc9;
}
</style>
