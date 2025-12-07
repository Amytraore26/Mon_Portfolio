<template>
  <div id="contact" class="min-h-screen bg-black text-white p-4 flex flex-col items-center pb-8">
    <div class="w-full max-w-6xl mt-8">
      <h1 class="text-4xl font-bold text-center bg-gradient-to-r from-blue-400 to-purple-500 text-transparent bg-clip-text mb-10">
        Contactez-moi
      </h1>

      <div class="flex flex-col md:flex-row gap-8 w-full">

        <!-- 🟦 Informations (gauche) -->
        <div class="bg-gray-900 p-8 rounded-3xl shadow-xl w-full md:w-1/2">
          <h2 class="text-2xl font-bold mb-8">Informations</h2>

          <div class="space-y-10">
            <div class="flex items-center gap-4 group">
              <div class="bg-blue-800 p-4 rounded-xl transform transition-transform duration-300 group-hover:translate-y-2">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-blue-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                </svg>
              </div>
              <div>
                <p class="text-gray-400">Email</p>
                <p>aminata.traore@epitech.eu</p>
              </div>
            </div>

            <div class="flex items-center gap-4 group">
              <div class="bg-green-900 p-4 rounded-xl transform transition-transform duration-300 group-hover:translate-y-2">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-green-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                </svg>
              </div>
              <div>
                <p class="text-gray-400">Téléphone</p>
                <p>+225 07 09 87 51 41</p>
              </div>
            </div>

            <div class="flex items-center gap-4 group">
              <div class="bg-purple-900 p-4 rounded-xl transform transition-transform duration-300 group-hover:translate-y-2">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-purple-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                </svg>
              </div>
              <div>
                <p class="text-gray-400">Localisation</p>
                <p>Abidjan, Côte d'Ivoire</p>
              </div>
            </div>
          </div>
        </div>

        <!-- 🟩 MAP (droite) -->
        <div class="rounded-3xl overflow-hidden shadow-xl w-full md:w-1/2">
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3977.0000000000005!2d-4.02775!3d5.33632!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x105ffbbc5fcd1b5d%3A0x0!2sYopougon,+Abidjan,+Côte%20d'Ivoire!5e0!3m2!1sfr!2sci!4v169_error!5m2!1sfr!2sci"
            width="100%"
            height="480"
            style="border:0;"
            allowfullscreen=""
            loading="lazy"
          ></iframe>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Contact"
};
</script>

<style scoped>
/* Si tu veux, tu peux ajouter ici des effets spéciaux ou glow pour tes titres */
</style>
