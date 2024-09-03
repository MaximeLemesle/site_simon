<template>
  <section
    class="programs__details flex flex-col items-center gap-8 bg-primary-100 neutre-900 px-36 py-24"
  >
    <h2 class="h2">Envoies moi un message</h2>

    <form id="contactForm" class="flex flex-col gap-6 w-4/5">
      <div class="name gap-6 flex">
        <div class="firstname flex flex-col gap-2 w-full">
          <label for="firstName" class="h4">Prénom</label>
          <input
            type="text"
            id="firstName"
            name="firstName"
            class="px-3 py-2 border w-full"
            placeholder="Prénom"
            required
          />
        </div>

        <div class="lastname flex flex-col gap-2 w-full">
          <label for="lastName" class="h4">Nom</label>
          <input
            type="text"
            id="lastName"
            name="lastName"
            class="px-3 py-2 border w-full"
            placeholder="Nom"
            required
          />
        </div>
      </div>

      <div class="phone flex flex-col gap-2 w-full">
        <label for="phone" class="h4">Numéro</label>
        <input
          type="tel"
          id="phone"
          name="phone"
          class="px-3 py-2 border w-full"
          placeholder="Numéro de téléphone"
          required
        />
      </div>

      <div class="msg-content flex flex-col gap-2 w-full">
        <label for="msg" class="h4">Message</label>
        <textarea
          id="msg"
          name="msg"
          class="px-3 py-2 border w-full h-48"
          placeholder="Écris ton message ici"
          required
        />
      </div>

    </form>

    <button class="btn btn-primary">Envoyer mon message</button>
  </section>
</template>