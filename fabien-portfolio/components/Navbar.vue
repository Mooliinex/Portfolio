<template>
  <div class="flex justify-center">
    <header
      class="px-1 py-4 bg-gray-900 shadow-2xl my-container sm:flex sm:justify-between sm:items-center sm:mt-8 sm:rounded-full"
    >
      <div class="flex items-center justify-between px-8">
        <img src="../assets/img/logo-name.png" alt="Logo Fabien" width="250" height="250">
          <title>logo-white</title>



        <div class="sm:hidden">
          <button
            @click="isOpen = !isOpen"
            type="button"
            class="block text-gray-500 hover:text-white focus:text-white focus:outline-none"
          >
          </button>
        </div>
      </div>
      <nav
        :class="isOpen ? 'block' : 'hidden'"
        class="px-8 py-4 sm:py-0 sm:block"
      >
        <div class="font-semibold text-xl text-white sm:flex">
          <a
            href="#"
            v-scroll-to="'#about'"
            class="block pt-3 sm:pt-0 sm:px-4 hover:text-indigo-300 "
          >À propos</a
          >
          <span class="hidden cursor-default sm:block sm:px-1">/</span>
          <a
            href="#"
            v-scroll-to="'#experience'"
            class="block pt-3 sm:pt-0 sm:px-4 hover:text-indigo-300"
          >Expériences</a
          >
          <span class="hidden cursor-default sm:block sm:px-1">/</span>
          <a
            href="#"
            v-scroll-to="'#projects'"
            class="block pt-3 sm:pt-0 sm:py-0 sm:px-4 hover:text-indigo-300"
          >Projets</a
          >
          <span class="hidden cursor-default sm:block sm:px-1">/</span>
          <a
            href="#"
            v-scroll-to="'#contact'"
            class="block pt-3 sm:pt-0 sm:px-4 hover:text-indigo-300"
          >Contact</a
          >
        </div>
      </nav>
    </header>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false
    };
  }
};
</script>

<style></style>
