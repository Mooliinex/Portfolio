<template>
  <div class="antialiased bg-gray-800">
    <Navbar />
    <nuxt />
  </div>
</template>

<script>
import Navbar from "~/components/Navbar";
export default {
  head() {
    return {
      title: "Fabien Le Fichoux / Web Developer"
    };
  },
  components: {
    Navbar,
  }
};
</script>

<style></style>
