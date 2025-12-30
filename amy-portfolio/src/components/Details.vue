<template>
  <div v-if="project" class="bg-gray-100 dark:bg-gray-800 py-64">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex flex-col md:flex-row -mx-4">

        <!-- IMAGE -->
        <div class="md:flex-1 px-4">
          <div class="h-[520px] rounded-lg bg-gray-200 dark:bg-gray-700 mb-4">
            <img
              class="w-full h-full object-contain rounded-lg"
              :src="project.image"
              :alt="project.title"
            />
          </div>

          <div class="flex -mx-2 mb-4">
            <div class="w-1/2 px-2">
              <button
                @click="$router.back()"
                class="w-full bg-gray-900 dark:bg-gray-600 text-white py-2 px-4 rounded-full font-bold hover:bg-gray-800 dark:hover:bg-gray-700"
              >
                ← Retour
              </button>
            </div>

            <div class="w-1/2 px-2">
              <a
                :href="project.github"
                target="_blank"
                class="block text-center w-full bg-gray-200 dark:bg-gray-700 text-gray-800 dark:text-white py-2 px-4 rounded-full font-bold hover:bg-gray-300 dark:hover:bg-gray-600"
              >
                GitHub
              </a>
            </div>
          </div>
        </div>

        <!-- DETAILS -->
        <div class="md:flex-1 px-4">
          <h2 class="text-3xl font-bold text-gray-800 dark:text-white mb-2">
            {{ project.title }}
          </h2>

          <p class="text-gray-600 dark:text-gray-300 text-sm mb-4">
            {{ project.shortDescription }}
          </p>

          <div class="flex mb-4 gap-6">
            <div>
              <span class="font-bold text-gray-700 dark:text-gray-300">Category:</span>
              <span class="text-gray-600 dark:text-gray-300 ml-1">
                {{ project.category }}
              </span>
            </div>
            <div>
              <span class="font-bold text-gray-700 dark:text-gray-300">Status:</span>
              <span class="text-gray-600 dark:text-gray-300 ml-1">
                {{ project.status }}
              </span>
            </div>
          </div>

          <!-- TECHNOLOGIES -->
          <div class="mb-4">
            <span class="font-bold text-gray-700 dark:text-gray-300">
              Technologies:
            </span>
            <div class="flex flex-wrap mt-2 gap-2">
              <span
                v-for="tech in project.technologies"
                :key="tech"
                class="bg-gray-300 dark:bg-gray-700 text-gray-700 dark:text-white py-1 px-3 rounded-full text-sm font-bold"
              >
                {{ tech }}
              </span>
            </div>
          </div>

          <!-- DESCRIPTION -->
          <div>
            <span class="font-bold text-gray-700 dark:text-gray-300">
              Project Description:
            </span>
            <p class="text-gray-600 dark:text-gray-300 text-sm mt-2">
              {{ project.description }}
            </p>
          </div>

        </div>
      </div>
    </div>
  </div>

  <!-- SI ID INVALIDE -->
  <div v-else class="text-center text-white py-32">
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
import redditImg from '../../assets/post.png'

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
          category: 'Web App',
          status: 'Completed',
          technologies: ['Vue.js', 'Laravel', 'API REST'],
          github: '#'
        },
        {
          id: '2',
          title: 'Web Integration',
          image: integrationImg,
          shortDescription: 'Intégration de maquette responsive.',
          description:
            'Reproduction fidèle d’une maquette Figma en site web responsive.',
          category: 'Frontend',
          status: 'Completed',
          technologies: ['HTML', 'CSS', 'JavaScript'],
          github: '#'
        },
        {
          id: '3',
          title: 'Admin Dashboard',
          image: dashboardImg,
          shortDescription: 'Dashboard de gestion.',
          description:
            'Interface administrateur avec CRUD complet.',
          category: 'Dashboard',
          status: 'Completed',
          technologies: ['Vue.js', 'CRUD'],
          github: '#'
        },
        {
          id: '4',
          title: 'ShowTime',
          image: showtimeImg,
          shortDescription: 'Réservation de tickets.',
          description:
            'Plateforme de réservation pour concerts et événements.',
          category: 'Web App',
          status: 'Completed',
          technologies: ['Nest.js', 'MongoDB'],
          github: '#'
        },
        {
          id: '5',
          title: 'Rotten Tomatoes Clone',
          image: rottenImg,
          shortDescription: 'Catalogue de films.',
          description:
            'Application web basée sur une API de films.',
          category: 'Web App',
          status: 'Completed',
          technologies: ['Next.js', 'API'],
          github: '#'
        },
        {
          id: '6',
          title: 'Post-It',
          image: postItImg,
          shortDescription: 'Gestion de notes.',
          description:
            'Application de notes avec création et suppression.',
          category: 'Productivité',
          status: 'Completed',
          technologies: ['Vue.js', 'API'],
          github: '#'
        },
        {
          id: '7',
          title: 'Yowl',
          image: yowlImg,
          shortDescription: 'Partage de liens.',
          description:
            'Partage de liens avec aperçu et KPI.',
          category: 'Web App',
          status: 'Completed',
          technologies: ['Laravel', 'MySQL'],
          github: '#'
        },
        {
          id: '8',
          title: 'TWP',
          image: twpImg,
          shortDescription: 'Gestion de tâches.',
          description:
            'Application inspirée de Trello.',
          category: 'Productivité',
          status: 'Completed',
          technologies: ['Vue.js'],
          github: '#'
        },
        {
          id: '9',
          title: 'Redditech',
          image: redditImg,
          shortDescription: 'App mobile de tâches.',
          description:
            'Application mobile connectée à l’API Trello.',
          category: 'Mobile App',
          status: 'Completed',
          technologies: ['React Native'],
          github: '#'
        }
      ]

      return projects.find(p => p.id === this.id)
    }
  }
}
</script>
