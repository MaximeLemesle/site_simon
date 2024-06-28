<template>
  <header class="bg-neutre-900 py-6 px-12 flex justify-between">
    <div class="logo">
      <nuxt-link to="/">
        <img src="@/assets/logo_simon-med-light.png" alt="Logo Simon" class="h-10" />
      </nuxt-link>
    </div>

    <nav class="navbar flex space-x-8">
      <nuxt-link to="/about" class="nav-font primary-100"> Qui suis je ? </nuxt-link>
      <nuxt-link to="/coaching" class="nav-font primary-100"> Coaching </nuxt-link>
      <nuxt-link to="/transformation" class="nav-font primary-100"> Transformation </nuxt-link>
      <nuxt-link to="/contact" class="nav-font primary-100"> Contact </nuxt-link>
    </nav>
  </header>
</template>
<style>
.navbar {
  text-transform: uppercase;
}
</style>
