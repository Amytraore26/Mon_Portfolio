<template>
  <section id="home" class="hero-3d min-h-[95vh] md:min-h-[80vh] flex items-center justify-center relative overflow-hidden">
    <div class="absolute inset-0" id="hero3d"></div>
    <div class="max-w-7xl mx-auto px-9 relative z-10">
      <div class="text-center">
        <div class="mb-8">
          <h1 class="text-5xl sm:text-6xl md:text-8xl font-black mb-6 parallax-element">
            <span class="bg-gradient-to-r from-purple-400 via-pink-400 to-cyan-400 bg-clip-text text-transparent text-glow">
                 Joelliane Aminata Traoré
            </span>
          </h1>
          <h2 class="text-xl sm:text-2xl md:text-3xl font-semibold text-gray-200 mb-6">
    Développeuse Web Fullstack
  </h2>
          <div class="text-lg sm:text-xl md:text-2xl text-gray-300 max-w-3xl mx-auto mb-8 parallax-element" data-speed="0.5">
            <span class="typing-text">
             Passionnée par la création de solutions digitales fiables et performantes.
            </span>
          </div>
        </div>
        
        <div class="flex flex-col sm:flex-row gap-6 justify-center items-center parallax-element" data-speed="0.3">
          <a href="CV_JOELLIANE_ANGE_AMINATA_TRAORÉ.pdf" download
             class="magnetic-button glass-morphism px-8 py-4 rounded-full text-lg font-semibold">
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
