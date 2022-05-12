<template>
  <div class="antialiased bg-gray-800">
    <Navbar />
    <nuxt />
    <Footer/>
  </div>
</template>

<script>
import Navbar from "../components/meta/Navbar";
import Footer from "../components/meta/Footer";
export default {
  head() {
    return {
      title: "Fabien Le Fichoux / Web Developer"
    };
  },
  components: {
    Navbar,
   Footer,
  }
};
</script>

<style></style>
