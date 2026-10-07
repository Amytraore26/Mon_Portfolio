<template>
  <div v-if="project" class="bg-gray-100 dark:bg-gray-800 min-h-screen pt-36 pb-12">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      
      <div class="flex flex-col md:flex-row gap-8">

        <!-- IMAGE -->
        <div class="md:flex-1">
          <div class="h-[420px] rounded-lg bg-gray-200 dark:bg-gray-700 mb-4 overflow-hidden">
            <img
              class="w-full h-full object-contain rounded-lg"
              :src="project.image"
              :alt="project.title"
            />
          </div>

          <!-- BOUTONS -->
          <div class="flex justify-center gap-4 mb-6">
  <button
    @click="$router.back()"
    :class="[
      'bg-gray-900 dark:bg-gray-600 text-white py-2 px-6 rounded-full font-bold hover:bg-gray-800 dark:hover:bg-gray-700',
      project.github && project.github !== '#' ? 'w-1/2' : 'w-full'
    ]"
  >
    ← Retour
  </button>

  <a
    v-if="project.github && project.github !== '#'"
    :href="project.github"
    target="_blank"
    rel="noopener noreferrer"
    class="w-1/2 text-center bg-gray-200 dark:bg-gray-700 text-gray-800 dark:text-white py-2 px-4 rounded-full font-bold hover:bg-gray-300 dark:hover:bg-gray-600"
  >
    Lien du projet
  </a>
</div>
        </div>

        <!-- DETAILS -->
        <div class="md:flex-1">

          <h2 class="text-3xl font-bold text-gray-800 dark:text-white mb-2">
            {{ project.title }}
          </h2>

          <p class="text-gray-600 dark:text-gray-300 mb-6">
            {{ project.shortDescription }}
          </p>

          <!-- TECHNOLOGIES -->
          <div class="mb-6">
            <h3 class="text-2xl font-bold text-gray-800 dark:text-white mb-3">
              Technologies :
            </h3>

            <div class="flex flex-wrap gap-2">
              <span
                v-for="tech in project.technologies"
                :key="tech"
                class="bg-gray-300 dark:bg-gray-700 text-gray-700 dark:text-white py-1.5 px-3 rounded-full text-sm font-medium"
              >
                {{ tech }}
              </span>
            </div>
          </div>

          <!-- DESCRIPTION -->
          <div class="mb-6">
            <h3 class="text-2xl font-bold text-gray-800 dark:text-white mb-2">
              Description du projet :
            </h3>

            <p class="text-gray-600 dark:text-gray-300 leading-7">
              {{ project.description }}
            </p>
          </div>

          <!-- CONTRIBUTION -->
          <div v-if="project.contribution">
            <h3 class="text-2xl font-bold text-gray-800 dark:text-white mb-2">
              Ma contribution :
            </h3>

            <p class="text-gray-600 dark:text-gray-300 leading-7">
              {{ project.contribution }}
            </p>
          </div>

        </div>
      </div>
    </div>
  </div>

  <!-- PROJET INTROUVABLE -->
  <div
    v-else
    class="text-center text-white py-32"
  >
    Projet introuvable
  </div>
</template>

<script>
import freeAdsImg from '../../assets/free.jpeg'
import integrationImg from '../../assets/1754919239625.jpeg'
import dashboardImg from '../../assets/dash.png'
import showtimeImg from '../../assets/show.jpeg'
import rottenImg from '../../assets/rott.jpeg'
import postItImg from '../../assets/post.png'
import yowlImg from '../../assets/yowl.png'
import twpImg from '../../assets/twp.png'
import yobaloImg from '../../assets/yobalo.jpeg'

export default {
  props: ['id'],

  computed: {
    project() {
      const projects = [
        {
          id: '1',
          title: 'Free Ads',
          image: freeAdsImg,
          shortDescription: 'Plateforme de publication d’annonces.',
          description:
            'Application web complète permettant aux utilisateurs de publier, rechercher et gérer des annonces.',
          // category: 'Web App',
          // status: 'Completed',
          technologies: ['Laravel','Tailwind css','CRUD','MySQL'],
          contribution: "Conception et développement du dashboard, de l’interface aux fonctionnalités. Mise en place de la gestion des annonces permettant de publier des annonces depuis le dashboard et de les afficher sur la page d’accueil. Chaque utilisateur dispose d’un dashboard personnalisé pour gérer ses propres annonces",
          github: '#'
        },
        {
          id: '2',
          title: 'Yowl',
          image: yowlImg,
          shortDescription: 'Partage de liens.',
          description:
            'Plateforme permettant de partager des liens externes et d’afficher automatiquement les informations associées, telles que le titre, la description, les images ou les vidéos et KPI.',
          contribution:
  'Participation à l’élaboration du cahier des charges et conception de la maquette sur Figma. Développement de l’ensemble de l’interface utilisateur, hors dashboard, ainsi que mise en place du système de commentaires permettant à chaque utilisateur de gérer ses propres commentaires.',
            category: 'Web App',
          status: 'Completed',
          technologies: ['Laravel', 'Tailwind css' ,'MySQL'],
          github: '#'
        },
       
        {
          id: '3',
          title: 'Yobalo',
          image: yobaloImg,
          shortDescription: 'App web de livraison de proximité.',
          description:
            "Yobalo est une plateforme de livraison de proximité qui met en relation les habitants d'un même quartier avec des livreurs situés à moins d'un kilomètre. L'objectif est de faciliter des livraisons rapides, locales et accessibles, tout en favorisant l'économie de quartier.",
          contribution:
              'Conception et intégration de la page « Livreur », avec mise en place d’une interface claire, moderne et responsive.',
            category: 'Web App',
          status: 'Completed, Liens du projet: OK', 
          technologies: ['WORDPRESS'],
          github: 'https://yobalo.com/'

         
        },
        {
          id: '4',
          title: 'Post-It',
          image: postItImg,
          shortDescription: 'Gestion de notes.',
          description:
            'Application de notes avec création et suppression.',
            contribution:
  'Conception et développement de l’interface utilisateur ainsi que mise en place du CRUD des notes.',
          category: 'Productivité',
          status: 'Completed, Liens du projet: OK', 
          technologies: ['Vue.js', 'Tailwind css' ,'API REST'],
          github: 'https://postit-ange.vercel.app/'
        },
        {
          id: '5',
          title: 'Admin Dashboard',
          image: dashboardImg,
          shortDescription: 'Dashboard de gestion.',
          description:
            'Dashboard intégrant différents services externes, notamment la météo, l’actualité et des contenus YouTube, à travers des API',
          contribution:
  'Conception et développement de l’ensemble de l’interface utilisateur et intégration du microservice météo à partir d’une API externe.',
            category: 'Dashboard',
          status: 'Completed',
          technologies: ['Vue.js','Tailwind css', 'API REST', 'Flask'],
          github: '#'
        },
        {
          id: '6',
          title: 'TWP',
          image: twpImg,
          shortDescription: 'Gestion de tâches.',
          description:
            'Application de gestion de tâches inspirée de Trello, permettant d’organiser les tâches au sein de différentes listes.',
          contribution:
  'Conception et développement de l’interface utilisateur ainsi que mise en place du CRUD des cartes de tâches au sein des différentes listes.',
            category: 'Productivité',
          status: 'Completed',
          technologies: ['Vue.js', 'Tailwind css', 'Wordpress'],
          github: '#'
        },
         {
          id: '7',
          title: 'Web Integration',
          image: integrationImg,
          shortDescription: 'Intégration de maquette responsive.',
          description:
            'Reproduction fidèle d’une maquette Figma en site web responsive.',
          contribution: "Intégration des cards et mise en place de leur responsive design pour assurer un affichage adapté aux différentes tailles d’écran.",
            category: 'Frontend',
          status: 'Completed, Liens du projet: OK', 
          technologies: ['HTML', 'CSS', 'JavaScript'],
          github: 'https://e-commerce-amy-sidoine.netlify.app/'
        },
        {
          id: '8',
          title: 'Rotten Tomatoes Clone',
          image: rottenImg,
          shortDescription: 'Catalogue de films.',
          description:
            'Application web basée sur une API de films.',
            contribution:
            'Conception et développement de l’ensemble de l’interface utilisateur du projet, avec intégration des données provenant de l’API.',
          category: 'Web App',
          status: 'Completed',
          technologies: ['Next.js', 'Tailwind css','API'],
          github: '#'
        },
        
        {
          id: '9',
          title: 'ShowTime',
          image: showtimeImg,
          shortDescription: 'Réservation de tickets.',
          description:
            'Plateforme de réservation pour concerts et événements.',
            contribution:
  'Conception et développement du dashboard permettant d’ajouter et de gérer les événements affichés sur la page d’accueil.',
          category: 'Web App',
          status: 'Completed',
          technologies: ['Nest.js', 'Tailwind css' ,'MongoDB'],
          github: '#'
        },
      ]

      return projects.find(p => p.id === this.id)
    }
  }
}
</script>
