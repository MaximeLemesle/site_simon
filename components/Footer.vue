<template>
  <footer>
    <section
      id="contact"
      class="bg-primary-300 px-40 py-12 flex justify-between items-center"
    >
      <div class="contact__info flex flex-col gap-8">
        <h2 class="h2 neutre-900">Me contacter</h2>

        <div class="contact__link flex flex-col gap-6">
          <div class="contact__link__item flex gap-6">
            <img
              src="@/assets/icons/tel.png"
              alt="Icon de téléphone"
              class="h-7"
            />
            <a href="#">01.23.45.67.89</a>
          </div>

          <div class="contact__link__item flex gap-6">
            <img src="@/assets/icons/mail.png" alt="Icon de mail" class="h-7" />
            <a href="#">simon@gmail.com</a>
          </div>

          <div class="contact__link__item">
            <a
              href="https://www.instagram.com/simon.videgrain/"
              class="flex gap-6"
            >
              <img
                src="@/assets/icons/insta.png"
                alt="Icon instagram"
                class="h-7"
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
        <div class="fake-img">
          <span class="h4">image de toi</span>
        </div>
      </div>
    </section>
    <section
      id="footer"
      class="bg-primary-500 px-40 py-12 flex flex-col items-center gap-8"
    >
      <div class="logo">
        <nuxt-link to="/">
          <img
            src="@/assets/logo_simon-full-light.png"
            alt="Logo Simon"
            class="h-24"
          />
        </nuxt-link>
      </div>

      <div class="footer__content flex justify-between w-full">
        <div class="footer__content__nav flex flex-col gap-4">
          <h4 class="h4 primary-900">Navigation</h4>
          <nuxt-link to="/about" class="primary-100 italic"
            >Qui-suis-je ?</nuxt-link
          >
          <nuxt-link to="/coaching" class="primary-100 italic"
            >Coaching</nuxt-link
          >
          <nuxt-link to="/transformation" class="primary-100 italic"
            >Transformation</nuxt-link
          >
          <nuxt-link to="/contact" class="primary-100 italic"
            >Contact</nuxt-link
          >
        </div>

        <div class="footer__content__contact flex flex-col gap-4">
          <h4 class="h4 primary-900">Contact</h4>
          <nuxt-link class="primary-100 italic">Mail</nuxt-link>
          <nuxt-link class="primary-100 italic">Numéro de tel</nuxt-link>
          <nuxt-link class="primary-100 italic">Adresse</nuxt-link>
        </div>

        <div class="footer__content__social flex flex-col gap-4">
          <h4 class="h4 primary-900">Réseaux sociaux</h4>
          <a
            href="https://www.instagram.com/simon.videgrain/"
            class="flex items-center gap-4 primary-100 italic"
          >
            <img
              src="@/assets/icons/instagram-light.png"
              alt="Icon instagram"
              class="h-6"
            />
            @simon.videgrain
          </a>
          <a href="#" class="flex items-center gap-4 primary-100 italic">
            <img
              src="@/assets/icons/tiktok-light.png"
              alt="Icon tiktok"
              class="h-6"
            />
            @simon.videgrain
          </a>
        </div>
      </div>

      <div class="footer__credit">
        <span class="footer-font neutre-0">
            ©Simon Coach Hybride - <a href="#">Paiement 100% sécurisé</a> - <a href="#">Mentions légales et Conditions générales de vente</a>
        </span>
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

.fake-img {
  height: 400px;
  width: 400px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #9d9d9d;
  color: #ffffff;
}
</style>
