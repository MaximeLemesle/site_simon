<template>
  <header class="bg-neutre-900 py-4 px-6 md:py-6 md:px-12 flex justify-between">
    <div class="logo">
      <nuxt-link to="/">
        <img src="@/assets/logo_simon-med-light.png" alt="Logo Simon" class="hidden sm:block h-10" />
        <img src="@/assets/logo_simon-small-light.png" alt="Logo Simon" class="sm:hidden h-10" />
      </nuxt-link>
    </div>

    <div class="lg:hidden h-10">
      <button @click="toggleMenu" class="primary-100 focus:outline-none">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-full w-10" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
        </svg>
      </button>
    </div>

    <nav class="navbar hidden lg:block lg:flex lg:space-x-8 lg:block">
      <nuxt-link to="/about" class="nav-font xl:text-2xl text-xl primary-100"> Qui suis je ? </nuxt-link>
      <nuxt-link to="/coaching" class="nav-font xl:text-2xl text-xl primary-100"> Coaching </nuxt-link>
      <nuxt-link to="/transformation" class="nav-font xl:text-2xl text-xl primary-100"> Transformation </nuxt-link>
      <nuxt-link to="/contact" class="nav-font xl:text-2xl text-xl primary-100"> Contact </nuxt-link>
    </nav>

    <!-- Fullscreen Mobile Menu Overlay -->
    <div v-if="isOpen" class="fixed inset-0 bg-neutre-900 flex flex-col items-center justify-center gap-12 z-50">
      <button @click="toggleMenu" class="absolute top-0 right-0 py-4 px-6 md:py-6 md:px-12 primary-100 focus:outline-none">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
      <nuxt-link to="/about" class="nav-font text-2xl primary-100" @click="toggleMenu"> Qui suis je ? </nuxt-link>
      <nuxt-link to="/coaching" class="nav-font text-2xl primary-100" @click="toggleMenu"> Coaching </nuxt-link>
      <nuxt-link to="/transformation" class="nav-font text-2xl primary-100" @click="toggleMenu"> Transformation </nuxt-link>
      <nuxt-link to="/contact" class="nav-font text-2xl primary-100" @click="toggleMenu"> Contact </nuxt-link>
    </div>
  </header>
</template>
<script setup>
import { ref } from 'vue';

const isOpen = ref(false);

const toggleMenu = () => {
  isOpen.value = !isOpen.value;
};
</script>