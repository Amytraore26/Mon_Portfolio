<template>
  <section id="home" class="hero-3d min-h-[100vh] md:min-h-[80vh] flex items-center justify-center relative overflow-hidden">
    <div class="absolute inset-0" id="hero3d"></div>
    <div class="max-w-7xl mx-auto px-9 relative z-10">
      <div class="text-center">
        <div class="mb-8">
          <h1 class="text-5xl sm:text-6xl md:text-8xl font-black mb-6 parallax-element">
            <span class="bg-gradient-to-r from-purple-400 via-pink-400 to-cyan-400 bg-clip-text text-transparent text-glow">
              Hey 👋 I am Joelliane Aminata TRAORE
            </span>
          </h1>
          <div class="text-lg sm:text-xl md:text-2xl text-gray-300 max-w-3xl mx-auto mb-8 parallax-element" data-speed="0.5">
            <span class="typing-text">
              Développeuse Frontend & Backend passionnée. Je transforme des idées en expériences digitales
            </span>
          </div>
        </div>
        
        <div class="flex flex-col sm:flex-row gap-6 justify-center items-center parallax-element" data-speed="0.3">
          <a href="CV_Aminata_TRAORE.pdf" download
             class="magnetic-button neon-border px-8 py-4 rounded-full text-lg font-semibold">
            Télécharger mon CV
          </a>
          <a href="#contact"
             class="magnetic-button glass-morphism px-8 py-4 rounded-full text-lg font-semibold">
            Contactez-moi
          </a>
        </div>
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
