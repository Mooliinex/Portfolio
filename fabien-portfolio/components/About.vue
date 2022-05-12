<template>
  <div>

<!--    SECTION About-->

  <section class="py-20 mx-auto xl:py-32 my-container" id="about">
    <div class="flex xl:max-w-6xl sm:items-center lg:items-start">
      <div class="w-full sm:w-2/3 lg:w-3/4 sm:pr-4">
        <div class="w-16 border-4 border-b border-white"></div>
        <span class="block pt-8 text-4xl font-semibold leading-none text-white sm:text-6xl">
            Fabien Le Fichoux
            <br/>Développeur Web
          </span>
        <div class="hidden md:block">
          <p class="max-w-xl pt-8 font-semibold text-indigo-300 sm:text-2xl">
            Passionné par la digitalisation et la création, je me suis réorienté vers le développement web.  En effet, j’ai déjà eu l’occasion de découvrir le monde du travail et de me former aux exigences de ce dernier.</p>
          <p class="max-w-xl pt-8 font-semibold text-indigo-300 sm:text-2xl">
           Polyvalent et flexible, je suis toujours désireux d'en savoir plus sur les technologies émergentes.</p>
          <p class="max-w-xl pt-8 font-semibold text-indigo-300 sm:text-2xl">
            J’espère que cette introduction vous donnera envie de me contacter et d’en savoir plus sur ce que je peux apporter à votre entreprise et à vos équipes.</p>
          <div class="pt-12">
            <button class="mr-4 btn btn-primary" ><a href="/CV-LE-FICHOUX-FABIEN.pdf" download >CV</a></button>

            <button class="btn btn-secondary" v-scroll-to="'#contact'">Contact</button>

          </div>
        </div>
      </div>
      <div class="flex items-center hidden md:block">
        <img
          class="h-98 bg-gray-900 rounded-3xl shadow-xl"
          src="../assets/img/unnamed.jpg"
          alt="Fabien Le Fichoux"
        />
      </div>
    </div>
    <div class="md:hidden">
      <p class="pt-8 text-lg font-semibold text-indigo-300 sm:text-xl">
        Passionné par la digitalisation et la création, je me suis réorienté vers le développement web.  En effet, j’ai déjà eu l’occasion de découvrir le monde du travail et de me former aux exigences de ce dernier.
        Polyvalent et flexible, je suis toujours désireux d'en savoir plus sur les technologies émergentes.
        J’espère que cette introduction vous donnera envie de me contacter et d’en savoir plus sur ce que je peux apporter à votre entreprise et à vos équipes.</p>
      <div class="pt-8">
        <button class="mr-4 btn btn-primary rounded-3xl" v-scroll-to="'#projects'">Mes projets</button>
        <button class="mt-4 btn btn-secondary rounded-3xl" v-scroll-to="'#contact'">Contact</button>
      </div>
    </div>
  </section>

<!--   SECTION Skill-->

  <section class="pt-10 bg-gray-700 sm:mt-24">
    <div class="mx-auto my-container">
      <div class="flex flex-wrap justify-center xl:-mx-3">
        <div
          v-for="(skill, index) in skills"
          :key="index"
          class="w-full my-3 lg:px-2 lg:-mt-40 xl:py-10 lg:w-1/3 xl:px-3"
        >
          <div
            class="relative overflow-hidden bg-gray-800 border-4 border-indigo-800 rounded-3xl shadow-xl h-skill-card"
          >
            <div class="relative z-50 flex flex-col items-center h-full px-4 py-12 text-center">
                <span
                  class="text-3xl font-semibold tracking-wide text-white uppercase lg:text-xl xl:text-3xl"
                >{{ skill.title }}</span>
              <p class="max-w-lg my-auto font-semibold text-lg text-indigo-300 ">{{ skill.description }}</p>
              <span
                class="block mt-auto font-bold text-center text-xl text-white uppercase lg:text-sm xl:text-xl"
              >{{ skill.tech }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  </div>
  </template>

<script>

export default {
  components: {

  },
  data() {
    return {
      skills: [
        {
          title: "Front-End Development",
          description:
          "lorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit ametlorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit amet ",
          tech: " JavaScript / Angular / Vue / Nuxt / React / HTML / CSS",
        },
        {
          title: "Back-End Development",
          description:
            "lorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit ametlorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit amet ",
          tech: "Node / Express  / MongoDB / MySQL",
        },
        {
          title: "Outils",
          description:
            "lorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit ametlorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit amet ",
          tech: "Jetbrain / GitHub  / Postman / Trello",
        },
      ],
    }
  },

};

</script>

<style scoped>

</style>
