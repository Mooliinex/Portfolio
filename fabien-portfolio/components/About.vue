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
          <p class="max-w-xl pt-8 font-semibold text-indigo-300 sm:text-xl">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aperiam, aspernatur dolore eum exercitationem illo ipsam iste numquam quibusdam sed sit tempora ut vero! Consequuntur cum qui quibusdam sapiente voluptas voluptates!
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ab, autem et facere fuga fugit illo, ipsa iure libero minima, nobis nostrum quod quos recusandae suscipit voluptatem? Beatae iste quibusdam similique.
          </p>
          <div class="pt-12">
            <button class="mr-4 btn btn-primary" v-scroll-to="'#projects'">Mes projets</button>
            <button class="btn btn-secondary" v-scroll-to="'#contact'">Contact</button>
          </div>
        </div>
      </div>
      <div class="flex items-center hidden lg:block">
        <img
          class="h-98 bg-gray-900 rounded-full shadow-xl"
          src="../assets/img/unnamed.jpg"
          alt="Fabien Le Fichoux"
        />
      </div>
    </div>
<!--    <div class="xl:hidden">-->
<!--      <p class="pt-8 text-lg font-semibold text-indigo-300 sm:text-xl">-->
<!--        lalalalalLorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquid delectus dolores esse eum illo molestiae nostrum quidem voluptatibus. Fuga illo ipsum laboriosam magni maiores nulla obcaecati quas quo repellendus totam.-->
<!--      </p>-->
<!--      <div class="pt-8">-->
<!--        <button class="mr-4 btn btn-primary" v-scroll-to="'#projects'">My Work</button>-->
<!--        <button class="mt-4 btn btn-secondary" v-scroll-to="'#contact'">Contact</button>-->
<!--      </div>-->
<!--    </div>-->
  </section>
  </template>

<script>
export default {
  name: "About"
}
</script>

<style scoped>

</style>
