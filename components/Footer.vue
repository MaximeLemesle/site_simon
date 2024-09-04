<template>
  <footer>
    <section
      id="contact"
      class="bg-primary-300 px-12 py-6 sm:px-24 sm:py-8 lg:px-40 lg:py-12 flex justify-between items-center"
    >
      <div class="contact__info flex flex-col items-center sm:items-start w-full gap-6 sm:gap-8">
        <h2 class="h2 neutre-900">Me contacter</h2>

        <div class="contact__link flex flex-col gap-4 md:gap-6">
          <div class="contact__link__item flex gap-4 lg:gap-6">
            <img
              src="@/assets/icons/tel.png"
              alt="Icon de téléphone"
              class="h-5 lg:h-7"
            />
            <a href="#">01.23.45.67.89</a>
          </div>

          <div class="contact__link__item flex gap-4 lg:gap-6">
            <img src="@/assets/icons/mail.png" alt="Icon de mail" class="h-5 lg:h-7" />
            <a href="#">simon@gmail.com</a>
          </div>

          <div class="contact__link__item">
            <a
              href="https://www.instagram.com/simon.videgrain/"
              class="flex gap-4 lg:gap-6"
            >
              <img
                src="@/assets/icons/insta.png"
                alt="Icon instagram"
                class="h-5 lg:h-7"
              />
              @simon.videgrain
            </a>
          </div>
        </div>

        <nuxt-link to="/contact" class="btn btn-primary"
          >Envoyer un message</nuxt-link
        >
      </div>

      <div class="contact__image">
        <div class="flex justify-center items-center bg-slate-400 neutre-0 hidden sm:block h-48 w-48 md:h-72 md:w-72 lg:h-96 lg:w-96">
          <span class="h4">image de toi</span>
        </div>
      </div>
    </section>
    <section
      id="footer"
      class="bg-primary-500 px-12 py-6 sm:px-24 sm:py-8 lg:px-40 lg:py-12 flex flex-col items-center gap-8"
    >
      <div class="logo">
        <nuxt-link to="/">
          <img
            src="@/assets/logo_simon-full-light.png"
            alt="Logo Simon"
            class="h-20 lg:h-24"
          />
        </nuxt-link>
      </div>

      <div class="footer__content flex flex-col items-center gap-6 sm:flex-row justify-between w-full">
        <div class="footer__content__nav flex flex-col gap-3 sm:gap-4">
          <h4 class="h4 primary-900">Navigation</h4>
          <nuxt-link to="/about" class="primary-100 italic text-sm md:text-base"
            >Qui-suis-je ?</nuxt-link
          >
          <nuxt-link to="/coaching" class="primary-100 italic text-sm	md:text-base"
            >Coaching</nuxt-link
          >
          <nuxt-link to="/transformation" class="primary-100 italic text-sm	md:text-base"
            >Transformation</nuxt-link
          >
          <nuxt-link to="/contact" class="primary-100 italic text-sm md:text-base"
            >Contact</nuxt-link
          >
        </div>

        <div class="footer__content__social flex flex-col gap-3 sm:gap-4">
          <h4 class="h4 primary-900">Réseaux sociaux</h4>
          <a
            href="https://www.instagram.com/simon.videgrain/"
            class="flex items-center gap-4 primary-100 italic text-sm	md:text-base"
          >
            <img
              src="@/assets/icons/instagram-light.png"
              alt="Icon instagram"
              class="h-6"
            />
            @simon.videgrain
          </a>
          <a href="#" class="flex items-center gap-4 primary-100 italic text-sm	md:text-base">
            <img
              src="@/assets/icons/tiktok-light.png"
              alt="Icon tiktok"
              class="h-6"
            />
            @simon.videgrain
          </a>
        </div>
      </div>

      <div class="footer__credit flex flex-wrap gap-4 justify-center">
        <span class="footer-font text-nowrap neutre-0">©Simon Coach Hybride</span>
        <span class="footer-font text-nowrap neutre-0"> - </span>
        <span class="footer-font text-nowrap neutre-0"><a href="#">Paiement 100% sécurisé</a></span>
        <span class="footer-font text-nowrap neutre-0"> - </span>
        <span class="footer-font text-nowrap neutre-0"><a href="#">Mentions légales et Conditions générales de vente</a></span>
      </div>
      <!-- crédit -->
    </section>
  </footer>
</template>
<style>
.contact__link__item {
  font-family: Dela Gothic One;
  letter-spacing: 0.5px;
  color: #ecf1f9;
}
</style>
