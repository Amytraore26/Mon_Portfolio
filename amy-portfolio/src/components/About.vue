<template>
  <section id="about" class="pt-16 overflow-hidden bg-black dark:bg-gray-800">
    <h1 class="text-4xl font-bold text-center bg-gradient-to-r from-purple-400 via-pink-400 to-cyan-400 bg-clip-text text-transparent text-glow">
      À Propos de moi
    </h1>

    <div class="px-4 mx-auto sm:px-6 lg:px-8 max-w-7xl">
      <div class="grid items-center grid-cols-1 md:grid-cols-2 gap-8 mt-8">

        <!-- Texte -->
        <div>
          <!-- <h2 class="text-3xl font-bold leading-tight text-white sm:text-4xl lg:text-5xl">
            I am Aminata TRAORE
          </h2> -->
          <p class="max-w-lg mt-4 text-xl text-center leading-relaxed text-white dark:text-gray-300 md:mt-8">
            Passionnée par la création digitale et l'univers du web. J'aime construire et donner vie à des projets qui allient simplicité et utilité. Motivée et déterminée.
            <br /><br />
            Mon objectif est de créer des plateformes modernes, fluides et centrées sur l'utilisateur, tout en continuant à évoluer et perfectionner ma manière de penser et de concevoir le web.
          </p>
        </div>

        <!-- Images -->
        <div class="relative">
          <img 
            class="absolute inset-x-0 bottom-0 -mb-48 -translate-x-1/2 left-1/2" 
            src="https://cdn.rareblocks.xyz/collection/celebration/images/team/1/blob-shape.svg" 
            alt="background shape" 
          />

          <img 
            class="relative w-full xl:max-w-lg xl:mx-auto 2xl:origin-bottom 2xl:scale-110" 
            src="../../assets/woman.png" 
            alt="Aminata TRAORE" 
          />
        </div>

      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "About",
};
</script>

<style scoped>
/* Glow text effect */
.text-glow {
  text-shadow: 0 0 8px rgba(255, 255, 255, 0.6);
}
</style>
