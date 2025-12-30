<template>
  <div class="bg-gray-900 rounded-xl overflow-hidden shadow-lg h-full hover:shadow-neon/20 transition-all tilt-effect" data-tilt data-tilt-max="5" data-tilt-glare="true">
    <img :src="image" :alt="title" class="w-full h-48 object-cover" />
    <div class="p-6">
      <h3 class="text-xl font-bold mb-2">{{ title }}</h3>
      <p class="opacity-80 mb-4">{{ description }}</p>
      <div class="flex flex-wrap gap-2 mb-4">
        <span v-for="tag in tagsArray" :key="tag" class="px-3 py-1 bg-glass rounded-full text-sm">{{ tag }}</span>
      </div>
<router-link :to="{ name: 'ProjectDetails', params: { id: projectId } }" class="text-red hover:underline">
  Détails →
</router-link>

   </div>
  </div>
</template>

<script>
export default {
  name: 'ProjectCard',
 props: {
  projectId: [Number, String], // <-- ajoute ça
  title: String,
  image: String,
  tags: String,
  description: { type: String, default: 'Description du projet.' }
},

  computed: {
    tagsArray() {
      return this.tags.split(',').map(t => t.trim());
    }
  }
}
</script>

<style scoped>
/* Optionnel : effet de verre */
.bg-glass {
  background: rgba(255,255,255,0.1);
  backdrop-filter: blur(5px);
}
</style>
