<template>
  <section id="projects" class="py-20 px-8">
    <div class="container mx-auto">
      <h2 class="text-4xl sm:text-5xl md:text-5xl font-bold mb-12 bg-gradient-to-r from-purple-400 via-pink-400 to-cyan-400 bg-clip-text text-transparent text-glow">
        Projets
      </h2>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <ProjectCard
  v-for="project in projects"
  :key="project.id"
  :project-id="project.id"
  :title="project.name"
  :image="project.image"
  :description="project.description"
  :tags="project.techs.join(', ')"
  :contribution="project.contribution"
  />

      </div>
    </div>
  </section>
</template>

<script>
import ProjectCard from './ProjectCard.vue'

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
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Projects",
  components: {
    ProjectCard
  },
  data() {
    return {
      projects: [
        { id: 1, name: "FREEADS", image: freeAdsImg, techs: ["Laravel","Tailwind css","MySQL"], description: "Plateforme permettant aux utilisateurs de publier, gérer et consulter des annonces de manière simple et intuitive.", contribution: "Conception et développement du dashboard, de l’interface aux fonctionnalités. Mise en place de la gestion des annonces permettant de publier des annonces depuis le dashboard et de les afficher sur la page d’accueil. Chaque utilisateur dispose d’un dashboard personnalisé pour gérer ses propres annonces."},
        { id: 2, name: "YOWL", image: yowlImg, techs: ["Laravel","Tailwind css","MySQL"], description: "Application web pour partager des liens externes avec suivi des KPI et commentaires." },
        { id: 3, name: "YOBALO", image: yobaloImg, techs: ["WordPress"], description: "Yobalo est une plateforme de livraison de proximité qui met en relation les habitants d'un même quartier avec des livreurs situés à moins d'un kilomètre." },
        { id: 4, name: "POST-IT", image: postItImg, techs: ["Vue.js","Tailwind css","API"], description: "Application de gestion et de rappel de notes pour organiser facilement ses rappels." },
        { id: 5, name: "DASHBOARD", image: dashboardImg, techs: ["React.js","API REST","Flask"], description: "Dashboard web interactif affichant plusieurs micro-services sous forme de widgets." },
        { id: 6, name: "TWP", image: twpImg, techs: ["Vue.js","Tailwind css","WordPress"], description: "Application web de gestion de tâches inspirée de Trello." },
        { id: 7, name: "INTEGRATION WEB", image: integrationImg, techs: ["HTML","CSS","JavaScript"], description: "Reproduction d'une maquette de site e-commerce en version responsive." },
        { id: 8, name: "ROTTEN-TOMATOES", image: rottenImg, techs: ["Next.js","Tailwind css","API"], description: "Site web de films pour parcourir, filtrer et trier les films par genre, date ou popularité." },
        { id: 9, name: "SHOW-TIME", image: showtimeImg, techs: ["Nest.js","Tailwind css","MongoDB"], description: "Site de réservation de tickets en ligne pour concerts et événements." },

      ]
    }
  }
}
</script>
