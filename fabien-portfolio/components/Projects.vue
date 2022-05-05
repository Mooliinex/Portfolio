<template>

<!--SECTION Projets-->

  <section class="py-20 bg-gray-700" id="projects">
    <div class="mx-auto my-container text-center">
      <h1 class="mb-6 text-3xl font-semibold tracking-widest text-white uppercase">Projects</h1>
      <div v-for="(project, index) in projects" :key="index" :class="{ 'mt-16': index > 0 }">
        <div class="relative flex items-center hidden rounded-xl xl:flex">
          <div class="z-10 w-3/5">
            <a
                v-if="project.link"
                class="cursor-pointer"
                :href="project.link"
                target="_blank"
              >
            <img
              class=" rounded-xl object-fit "
              :src="require('~/assets/img/project/' + project.img + '-pro.jpg')"
            />
                </a>
          </div>
          <div class="absolute z-40 w-3/5 pl-16" style="right: 0">
            <div class="p-8 bg-gray-800 border-2 border-indigo-900 rounded-xl shadow-xl">
                <span class="text-2xl font-semibold text-white uppercase">
                  {{
                    project.title
                  }}
                </span>
              <p class="pt-4 text-xl font-semibold text-indigo-300">{{ project.description }}</p>

              <span
                class="block pt-6 text-lg font-semibold text-white uppercase"
              >{{ project.technologies }}</span>
            </div>
          </div>
        </div>

<!--   RESPONSIVE     -->

        <div class="flex justify-center xl:hidden ">
          <div class="overflow-hidden bg-gray-800 rounded-xl">
            <a
              v-if="project.link"
              class="cursor-pointer"
              :href="project.link"
              target="_blank"
            >
            <img
              class="object-cover w-full"
              :src="require('~/assets/img/project/' + project.img + '.jpg')"
            />
            </a>
            <div class="flex flex-col justify-center px-10 pt-5 pb-10">
                <span class="text-2xl font-semibold text-white uppercase">
                  {{
                    project.title
                  }}
                </span>
              <p class="pt-4 text-xl font-semibold text-indigo-300">{{ project.description }}</p>

              <span
                class="block pt-6 text-xl font-semibold text-white uppercase"
              >{{ project.technologies }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

</template>

<script>

export default {
  components: {

  },
  data() {
    return {
      projects: [{
        title: "CandyShop",
        technologies: "Angular / Bootstrap / MongoDB / Node / Express",
        link: "http://candy.wac.ovh/",
        img: "candy",
        description:
          " lorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit ametlorem ipsum dolor sit ametlorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit ametlorem ipsum dolor sit ametlorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit ametlorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit amet       "
      },
        {
        title: "Meetyc",
      technologies: "Angular / Bootstrap / MongoDB / Node / Express",
      link: "https://github.com/Mooliinex/Projet-My_Meetic",
      img: "meetyc",
      description:
    " lorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit ametlorelorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit ametlorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit amet       "
  },
        {
          title: "Cinema",
          technologies: "Angular / Bootstrap / MongoDB / Node / Express",
          link: "https://github.com/Mooliinex/Projet-My_Meetic",
          img: "cinema",
          description:
            " lorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit ametlorelorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit ametlorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit amet       "
        },
        {
          title: "Puissance 4",
          technologies: "Angular / Bootstrap / MongoDB / Node / Express",
          link: "https://github.com/Mooliinex/Projet-My_Meetic",
          img: "game",
          description:
            " lorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit ametlorelorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit ametlorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit amet       "
        },
        {
          title: "Morpion",
          technologies: "Angular / Bootstrap / MongoDB / Node / Express",
          link: "https://github.com/Mooliinex/Projet-My_Meetic",
          img: "win",
          description:
            " lorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit ametlorelorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit ametlorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit amet       "
        },

      ]
    }
  }

};

</script>

<style scoped>

</style>
