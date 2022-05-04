<template>

<!--SECTION Projets-->

  <section class="py-20 bg-gray-700" id="projects">
    <div class="mx-auto my-container text-center">
      <h1 class="mb-6 text-3xl font-semibold tracking-widest text-white uppercase">Projects</h1>
      <div v-for="(project, index) in projects" :key="index" :class="{ 'mt-16': index > 0 }">
        <div class="relative flex items-center hidden rounded xl:flex">
          <div class="z-10 w-3/5">

            <img
              class="rounded-t object-fit"
              :src="require('~/assets/img/project/' + project.img + '-pro.jpg')"
            />

          </div>
          <div class="absolute z-40 w-3/5 pl-16" style="right: 0">
            <div class="p-8 bg-gray-800 border-2 border-indigo-500 rounded shadow-xl">
                <span class="text-xl font-semibold text-white uppercase">
                  {{
                    project.title
                  }}
                </span>
              <p class="pt-4 text-lg text-indigo-300">{{ project.description }}</p>
              <div class="flex items-center py-5">
                <a
                  v-if="project.github"
                  class="cursor-pointer"
                  :href="project.github"
                  target="_blank"
                >
                  <svg
                    class="w-6 h-6 mr-3 text-white fill-current hover:text-indigo-300"
                    viewBox="0 0 24 24"
                  >
                    <defs />
                    <path
                      d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"
                    />
                  </svg>
                </a>
                <a class="cursor-pointer" :href="project.link" target="_blank">
                  <svg
                    class="w-6 h-6 text-white fill-current hover:text-indigo-300"
                    viewBox="0 0 24 24"
                  >
                    <defs />
                    <path
                      d="M4.06 13a8 8 0 005.18 6.51A18.5 18.5 0 018.02 13H4.06zm0-2h3.96a18.5 18.5 0 011.22-6.51A8 8 0 004.06 11zm15.88 0a8 8 0 00-5.18-6.51A18.5 18.5 0 0115.98 11h3.96zm0 2h-3.96a18.5 18.5 0 01-1.22 6.51A8 8 0 0019.94 13zm-9.92 0c.16 3.95 1.23 7 1.98 7s1.82-3.05 1.98-7h-3.96zm0-2h3.96c-.16-3.95-1.23-7-1.98-7s-1.82 3.05-1.98 7zM12 22a10 10 0 110-20 10 10 0 010 20z"
                      class="heroicon-ui"
                    />
                  </svg>
                </a>
              </div>
              <span
                class="block pt-6 text-xs font-semibold text-white uppercase"
              >{{ project.technologies }}</span>
            </div>
          </div>
        </div>

<!--   RESPONSIVE     -->

        <div class="flex justify-center xl:hidden">
          <div class="overflow-hidden bg-gray-800 rounded">
            <img
              class="object-cover w-full"
              :src="require('~/assets/img/project/' + project.img + '-pro.jpg')"
            />
            <div class="flex flex-col justify-center px-10 pt-5 pb-10">
                <span class="text-2xl font-semibold text-white uppercase">
                  {{
                    project.title
                  }}
                </span>
              <p class="pt-4 text-lg text-indigo-300">{{ project.description }}</p>
              <div class="flex items-center py-5">
                <a
                  v-if="project.github"
                  class="cursor-pointer"
                  :href="project.github"
                  target="_blank"
                >
                  <svg
                    class="w-6 h-6 mr-3 text-white fill-current hover:text-indigo-300"
                    viewBox="0 0 24 24"
                  >
                    <defs />
                    <path
                      d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"
                    />
                  </svg>
                </a>
                <a class="cursor-pointer" :href="project.link" target="_blank">
                  <svg
                    class="w-6 h-6 text-white fill-current hover:text-indigo-300"
                    viewBox="0 0 24 24"
                  >
                    <defs />
                    <path
                      d="M4.06 13a8 8 0 005.18 6.51A18.5 18.5 0 018.02 13H4.06zm0-2h3.96a18.5 18.5 0 011.22-6.51A8 8 0 004.06 11zm15.88 0a8 8 0 00-5.18-6.51A18.5 18.5 0 0115.98 11h3.96zm0 2h-3.96a18.5 18.5 0 01-1.22 6.51A8 8 0 0019.94 13zm-9.92 0c.16 3.95 1.23 7 1.98 7s1.82-3.05 1.98-7h-3.96zm0-2h3.96c-.16-3.95-1.23-7-1.98-7s-1.82 3.05-1.98 7zM12 22a10 10 0 110-20 10 10 0 010 20z"
                      class="heroicon-ui"
                    />
                  </svg>
                </a>
              </div>
              <span
                class="block pt-6 text-xs font-semibold text-white uppercase"
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
      projects: [
        {
          title: "lorem ipsum dolor sit amet",
          technologies: "Vue / Nuxt / Bootstrap-Vue / MongoDB / Node / Express",
          link: "https://mooliinex.github.io/",
          img: "unnamed",
          description:
" lorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit ametlorem ipsum dolor sit amet, consectetur lorem ipsum dolor sit amet       "
        },

      ]
    }
  }

};

</script>

<style scoped>

</style>
