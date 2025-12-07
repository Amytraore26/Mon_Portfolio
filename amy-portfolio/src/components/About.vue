<template>
  <section id="about" class="pt-1 overflow-hidden bg-black md:pt-0 sm:pt-16 2xl:pt-16">
    <h1 class="text-4xl sm:text-5xl font-bold text-center bg-gradient-to-r from-purple-400 via-pink-400 to-cyan-400 bg-clip-text text-transparent text-glow">
      À Propos de moi
    </h1>

    <div class="px-4 mx-auto sm:px-6 lg:px-8 max-w-7xl">
      <div class="grid items-center grid-cols-1 md:grid-cols-2 gap-8">

        <div>
          <h2 class="mt-9 text-1xl sm:text-2xl lg:text-3xl font-bold leading-tight text-white">
            Développeuse Full-Stack
            <br class="block sm:hidden" />
          </h2>

          <p class="max-w-lg mt-6 sm:mt-9 text-base sm:text-xl leading-relaxed text-white">
 Passionnée par la création d'applications web modernes, performantes et intuitives.
Je conçois des interfaces fluides et des systèmes complets (front + back) capables de répondre aux besoins réels des utilisateurs.
Curieuse, dynamique et capable de travailler sous pression, j'aime apprendre, comprendre et bâtir des solutions qui simplifient la vie.          </p>
        </div>

        <div class="relative">
          <img class="absolute inset-x-0 bottom-0 -mb-48 -translate-x-1/2 left-1/2" src="https://cdn.rareblocks.xyz/collection/celebration/images/team/1/blob-shape.svg" alt="" />
          <img class="relative w-full xl:max-w-lg xl:mx-auto 3xl:origin-bottom 2xl:scale-110" src="../../assets/woman.png" alt="" />
        </div>

      </div>
    </div>
  </section>
</template>

<style scoped>
.text-glow {
  text-shadow: 0 0 8px rgba(255, 255, 255, 0.6);
}
</style>
