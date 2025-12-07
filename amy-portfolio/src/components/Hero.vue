<template>
<section id="home" class="hero-3d min-h-screen flex items-center justify-center relative overflow-hidden">
<div class="max-w-7xl mx-auto px-6 relative z-10 text-center">
<h1 class="text-5xl md:text-7xl font-black mb-6">
<span class="bg-gradient-to-r from-purple-400 via-pink-400 to-cyan-400 bg-clip-text text-transparent">Hey 👋 I am Aminata TRAORE</span>
</h1>
<p class="text-xl md:text-2xl text-gray-300 max-w-3xl mx-auto mb-8">Développeuse Frontend & Backend passionnée. Je transforme des idées en expériences digitales.</p>
<div class="flex flex-col sm:flex-row gap-6 justify-center items-center">
<a href="../public/CV_Aminata_TRAORE.pdf" download="CV_Aminata_Traore.pdf" class="magnetic-button neon-border px-8 py-4 rounded-full text-lg font-semibold">
  Télécharger mon CV
</a><a href="#contact" class="magnetic-button glass-morphism px-8 py-4 rounded-full text-lg font-semibold">Contactez-moi</a>
</div>
</div>
</section>
</template>


<script>
export default {
name: 'Hero',
mounted() {
// small parallax / animation hooks can go here
}
}
</script>