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
             alt="image projet"/>
                </a>
          </div>
          <div class="absolute z-40 w-3/5 pl-16" style="right: 0">
            <div class="p-8 bg-gray-800 border-2 border-indigo-900 rounded-xl shadow-xl">
                <span class="text-xl font-semibold text-white uppercase">
                  {{
                    project.title
                  }}
                </span>
              <p class="pt-4 text-lg text-indigo-300">{{ project.description }}</p>

              <span
                class="block pt-6 text-xs font-semibold text-white uppercase"
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
             alt="image projet"/>
            </a>
            <div class="flex flex-col justify-center px-10 pt-5 pb-10">
                <span class="text-2xl font-semibold text-white uppercase">
                  {{
                    project.title
                  }}
                </span>
              <p class="pt-4 text-lg text-indigo-300">{{ project.description }}</p>

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
      projects: [{
        title: "CandyShop",
        technologies: "Angular / Bootstrap / MongoDB / Node / Express",
        link: "http://candy.wac.ovh/",
        img: "candy",
        description:
          "Création d'un site e-commerce dans le but de comprendre et d'utiliser le mécanisme MVCS (Model/View/Controller/Service). Projet de 3 semaines réalisé après 5 mois de formation . Fini à 70% manque le dahsboard admin et la validation / historique commande. "
      },
        {
        title: "Meetyc",
      technologies: "HTML5 / CSS / JQuery / PHP / POO / Express",
      link: "https://github.com/Mooliinex/Projet-My_Meetic",
      img: "meetyc",
      description:
    "Création d'un site de rencontres à la manière d’un Meetic. Projet de 2 semaine réalisé après 4 mois de formation"
  },
        {
          title: "Morpion",
          technologies: "JS / LibrairieJQuery / Algorithmie / Trois dimensions ",
          link: "https://github.com/Mooliinex/Colle-Morpion",
          img: "win",
          description:
            "Examen de 4h pour développer un jeu de morpion. Réalisé après 3 de formation."
        },
        {
          title: "Puissance 4",
          technologies: "JS / LibrairieJQuery / Algorithmie / Jeu ",
          link: "https://github.com/Mooliinex/Projet-Puissance4",
          img: "game",
          description:
            "Réalisation un jeu en utilisant la librairie jQuery reprenant les règles du célèbre jeu de Puissance 4.  Projet de 2 semaine réalisé après 3 mois de formation "
        },
        {
          title: "CSS generator",
          technologies: "PHP / Gestion des fichiers en PHP / Spritesheets CSS / UNIX  ",
          link: "https://github.com/Mooliinex/Projet-CSS-Generator",
          img: "sprite",
          description:
            "Au départ, nous avons un dossier contenant plusieurs images au format PNG. L’idée principale du projet est de développer un programme, qui concatène toutes ces images en un seul sprite. L’idée secondaire est de générer le fichier CSS représentant cette concaténation. Projet de 3 semaines réalisé après 2 mois de formation "
        },
        {
          title: "Cinema",
          technologies: "HTML5 / CSS / JS / PHP / SQL ",
          link: "https://github.com/Mooliinex/Projet-My_cinema",
          img: "cinema",
          description:
            " À partir de la base de données MySQL fournie création d'un site qui permet d’interagir avec cette dernière. Projet de 1 semaine réalisé après 1 mois de formation ."
        },
        {
          title: "Maquette HTML",
          technologies: "HTML5 / CSS / JS / PHP / SQL ",
          link: "https://github.com/Mooliinex/Maquette-HTML",
          img: "img",
          description:
            " À partir de la base de données MySQL fournie création d'un site qui permet d’interagir avec cette dernière. Projet de 1 semaine réalisé après 1 mois de formation ."
        },

      ]
    }
  }

};

</script>

<style scoped>

</style>
