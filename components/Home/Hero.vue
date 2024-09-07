<template>
  <section class="hero p-8 sm:px-8 sm:py-12 lg:px-56 lg:pt-36 lg:pb-24 flex flex-col items-center gap-8">
    <h1 class="h1 primary-100 text-center">
      Phrase mettant en avant ta vision
    </h1>
    <div class="quote primary-100 w-3/5 text-center">
      <p>
        “Le secret du changement c’est de concentrer toute votre énergie non pas
        a lutter contre le passé mais a construire l’avenir.”
      </p>
      <p class="italic">- Socrate -</p>
    </div>
    <nuxt-link to="/contact" class="btn btn-primary"> Me contacter </nuxt-link>
  </section>
</template>
<style>
.hero {
  background-image: url("@/assets/bg-home.svg");
  background-size: cover;
}
</style>