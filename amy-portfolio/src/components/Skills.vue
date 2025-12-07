<template>
<section id="skills" class="pt-16 pb-12 bg-black">
<div class="max-w-7xl mx-auto px-6">
<h2 class="text-4xl font-bold text-center bg-gradient-to-r from-purple-400 via-pink-400 to-cyan-400 bg-clip-text text-transparent text-glow mb-14">Compétences</h2>
<h3 class="text-2xl font-semibold mb-6">Langages</h3>
<div class="grid grid-cols-2 md:grid-cols-4 gap-6 mb-10">
<div v-for="lang in languages" :key="lang.name" class="p-4 bg-gray-900 rounded-xl text-center">
<img :src="lang.icon" :alt="lang.name" class="w-12 h-12 mx-auto mb-2" />
<div class="font-semibold">{{ lang.name }}</div>
</div>
</div>


<h3 class="text-2xl font-semibold mb-6">Frameworks & Tools</h3>
<div class="grid grid-cols-2 md:grid-cols-4 gap-6">
<div v-for="fw in frameworks" :key="fw.name" class="p-4 bg-gray-900 rounded-xl text-center">
<img :src="fw.icon" :alt="fw.name" class="w-12 h-12 mx-auto mb-2" />
<div class="font-semibold">{{ fw.name }}</div>
</div>
</div>


<h3 class="text-2xl font-semibold mt-10 mb-6">Outils</h3>
<div class="grid grid-cols-2 md:grid-cols-5 gap-6">
<div v-for="tool in tools" :key="tool.name" class="p-4 bg-gray-900 rounded-xl text-center">
<img :src="tool.icon" :alt="tool.name" class="w-12 h-12 mx-auto mb-2" />
<div class="font-semibold">{{ tool.name }}</div>
</div>
</div>
</div>
</section>
</template>


<script>
export default {
name: 'Skills',
props: ['languages', 'frameworks', 'tools']
}
</script>