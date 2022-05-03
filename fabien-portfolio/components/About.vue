<template>
  <section class="py-20 mx-auto xl:py-32 my-container" id="about">
    <div class="flex xl:max-w-6xl sm:items-center lg:items-start">
      <div class="w-full sm:w-2/3 lg:w-3/4 sm:pr-4">
        <div class="w-16 border-4 border-b border-white"></div>
        <span class="block pt-8 text-4xl font-semibold leading-none text-white sm:text-6xl">
            Fabien Le Fichoux
            <br/>Web Developer
          </span>
        <div class="hidden md:block">
          <p class="max-w-xl pt-8 font-semibold text-indigo-300 sm:text-2xl">
            Passionné par la digitalisation et la création, je me suis réorienté vers le développement web.  En effet, j’ai déjà eu l’occasion de découvrir le monde du travail et de me former aux exigences de ce dernier.</p>
          <p class="max-w-xl pt-8 font-semibold text-indigo-300 sm:text-2xl">
           Polyvalent et flexible, je suis toujours désireux d'en savoir plus sur les technologies émergentes.</p>
          <p class="max-w-xl pt-8 font-semibold text-indigo-300 sm:text-2xl">
            J’espère que cette introduction vous donnera envie de me contacter et d’en savoir plus sur ce que je peux apporter à votre entreprise et à vos équipes.</p>

          <div class="pt-12">
            <button class="mr-4 btn btn-primary" v-scroll-to="'#projects'">Mes projets</button>
            <button class="btn btn-secondary" v-scroll-to="'#contact'">Contact</button>
          </div>
        </div>
      </div>
      <div class="flex items-center hidden md:block">
        <img
          class="h-98 bg-gray-900 rounded-full shadow-xl"
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

      </p>
      <div class="pt-8">
        <button class="mr-4 btn btn-primary" v-scroll-to="'#projects'">Mes projets</button>
        <button class="mt-4 btn btn-secondary" v-scroll-to="'#contact'">Contact</button>
      </div>
    </div>
  </section>
  </template>

<script>
export default {
  name: "About"
}
</script>

<style scoped>

</style>
