<template>
  <section class="container mx-auto px-4 py-16 md:py-24">
    <h2 class="text-4xl sm:text-5xl md:text-5xl font-bold text-center dark:text-white mb-12 sm:mb-20 text-center bg-gradient-to-r from-purple-400 via-pink-400 to-cyan-400 bg-clip-text text-transparent text-glow">
      Formation
    </h2>

    <div class="relative">
      <!-- Central Vertical Line -->
<div class="absolute left-1/2 transform -translate-x-1/2 h-full w-[2px] md:w-1 bg-blue-200 dark:bg-blue-900/50"></div>

      <!-- Timeline Items Container -->
      <div class="space-y-12 md:space-y-24">
        <!-- Item 1 -->
        <div class="timeline-item flex flex-col md:flex-row items-center md:justify-between relative">
          <!-- Left Side Content (Desktop) -->
          <div class="hidden md:block md:w-1/2 pr-12"></div>

          <!-- Icon -->
          <div class="flex md:absolute left-1/2 transform md:-translate-x-1/2 mb-4 md:mb-0 z-10">
            <div class="flex items-center justify-center w-12 h-12 rounded-full bg-blue-500 text-white border-4 border-white dark:border-gray-900 shadow-lg">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z" />
              </svg>
            </div>
          </div>

          <!-- Right Side Card -->
          <div class="ml-0 md:ml-12 md:w-1/2 w-full">
            <div class="timeline-card bg-gray-900 dark:bg-gray-800 rounded-2xl shadow-lg p-4 sm:p-6 border-l-4 border-blue-500 transform transition-all duration-500 hover:scale-[1.02]">
              <p class="text-xs sm:text-sm font-semibold text-blue-600 dark:text-blue-400">Juin - Décembre 2025</p>
              <h3 class="text-lg sm:text-xl font-bold text-white dark:text-white mt-2">Développement fullstack</h3>
              <p class="text-sm sm:text-base text-white dark:text-white mt-2 sm:mt-4">We.Code</p>
            </div>
          </div>
        </div>

        <!-- Item 2 -->
        <div class="timeline-item flex flex-col md:flex-row items-center md:justify-between relative">
          <div class="md:w-1/2 md:pr-12 w-full order-2 md:order-1">
            <div class="timeline-card bg-gray-900 dark:bg-gray-800 rounded-2xl shadow-lg p-4 sm:p-6 border-l-4 border-green-500 transform transition-all duration-500 hover:scale-[1.02]">
              <p class="text-xs sm:text-sm font-semibold text-green-600 dark:text-green-400">2023 - À présent</p>
              <h3 class="text-lg sm:text-xl font-bold text-white dark:text-white mt-2">Licence développement d'application et e-service</h3>
              <p class="text-sm sm:text-base text-white dark:text-white mt-2 sm:mt-4">Université Virtuelle de Côte d'Ivoire</p>
            </div>
          </div>

          <!-- Icon -->
          <div class="flex md:absolute left-1/2 transform md:-translate-x-1/2 mb-4 md:mb-0 z-10 order-1 md:order-2">
            <div class="flex items-center justify-center w-12 h-12 rounded-full bg-green-500 text-white border-4 border-white dark:border-gray-900 shadow-lg">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
              </svg>
            </div>
          </div>
        </div>

        <!-- Item 3 -->
        <div class="timeline-item flex flex-col md:flex-row items-center relative">
          <div class="hidden md:block md:w-1/2 pr-12"></div>
          <div class="flex md:absolute left-1/2 transform md:-translate-x-1/2 mb-4 md:mb-0 z-10">
            <div class="flex items-center justify-center w-12 h-12 rounded-full bg-purple-500 text-white border-4 border-white dark:border-gray-900 shadow-lg">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14.752 11.168l-3.197-2.132A1 1 0 0010 9.87v4.263a1 1 0 001.555.832l3.197-2.132a1 1 0 000-1.664z" />
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
            </div>
          </div>
          <div class="ml-0 md:ml-12 md:w-1/2 w-full">
            <div class="timeline-card bg-gray-900 dark:bg-gray-800 rounded-2xl shadow-lg p-4 sm:p-6 border-l-4 border-purple-500 transform transition-all duration-500 hover:scale-[1.02]">
              <p class="text-xs sm:text-sm font-semibold text-purple-600 dark:text-purple-400">2022 - 2023</p>
              <h3 class="text-lg sm:text-xl font-bold text-white dark:text-white mt-2">Baccalauréat D</h3>
              <p class="text-sm sm:text-base text-white dark:text-white mt-2 sm:mt-4">Lycée Moderne de Port Bouet</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Timeline',
}
</script>
