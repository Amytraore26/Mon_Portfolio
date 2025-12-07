<template>
<div class="bg-gray-900 rounded-xl overflow-hidden shadow-lg h-full">
<img :src="image" :alt="title" class="w-full h-48 object-cover" />
<div class="p-6">
<h3 class="text-xl font-bold mb-2">{{ title }}</h3>
<p class="opacity-80 mb-4">{{ description }}</p>
<div class="flex flex-wrap gap-2 mb-4">
<span v-for="tag in tagsArray" :key="tag" class="px-3 py-1 bg-glass rounded-full text-sm">{{ tag }}</span>
</div>
</div>
</div>
</template>


<script>
export default {
name: 'ProjectCard',
props: {
title: String,
image: String,
tags: String,
description: { type: String, default: 'Description du projet.' }
},
computed: {
tagsArray() {
return this.tags.split(',').map(t => t.trim())
}
}
}
</script>