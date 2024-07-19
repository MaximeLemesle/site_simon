<template>
  <section class="about px-36 py-14 flex items-center gap-12 bg-neutre-0">
    <img src="@/assets/fake-img-simon.png" alt="Fausse image" class="h-96" />
    <div class="content flex flex-col gap-8 items-left">
        <h2 class="h2 neutre-900">Simon Coach Hybride</h2>

        <p class="neutre-900">
        Je suis coach diplômé d'un BPJEPS mention musculation/haltérophilie obtenu
        au CREPS de Montpellier. J'ai à cœur de vous accompagner de la meilleure
        façon possible pour réaliser vos objectifs, qu'il s'agisse de la reprise
        d'une activité physique, de la perte de poids, de la prise de masse ou de
        la réalisation d'une performance physique.
        </p>

        <nuxt-link to="/about" class="btn btn-secondary">
            En apprendre plus sur ma moi
        </nuxt-link>
    </div>
  </section>
</template>
