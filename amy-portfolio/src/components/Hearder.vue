<!-- eslint-disable vue/multi-word-component-names -->
<template>
<body class="bg-black text-white overflow-x-hidden">
  <!-- Interactive Cursor -->
  <div class="interactive-cursor" id="cursor"></div>
  
  <!-- Scroll Progress -->
  <div class="scroll-progress" id="scrollProgress"></div>
  
  <!-- Particle System -->
  <div class="particle-container" id="particleContainer"></div>
  
  <!-- Floating Orbs -->
  <div class="floating-orb w-96 h-96 bg-gradient-to-r from-purple-400 to-pink-400 top-10 -left-48 opacity-20"></div>
  <div class="floating-orb w-80 h-80 bg-gradient-to-r from-blue-400 to-cyan-400 top-96 -right-40 opacity-20" style="animation-delay: -4s;"></div>
  <div class="floating-orb w-64 h-64 bg-gradient-to-r from-green-400 to-blue-400 bottom-20 left-1/2 opacity-20" style="animation-delay: -2s;"></div>

  <!-- Navigation -->
  <nav class="glass-morphism fixed w-full z-50 transition-all duration-500 py-4" id="navbar">
    <div class="max-w-7xl mx-auto px-6">
      <div class="flex justify-between items-center">
        <div class="flex items-center space-x-4">
          <div class="text-2xl font-bold bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent hover:scale-110 transition-transform duration-300">
            <a href="#home" class="flex items-center">
              <span class="animate-bounce mr-2">🚀</span>
              <span class="typing-animation">TAAJ</span>
            </a>
          </div>
        </div>
        <div class="hidden lg:flex items-center space-x-8">
          <a href="#home" class="nav-link relative group px-4 py-2 rounded-full transition-all duration-300 hover:bg-white/10">
            Acceuil
            <span class="absolute inset-0 rounded-full bg-gradient-to-r from-purple-400 to-pink-400 opacity-0 group-hover:opacity-20 transition-opacity"></span>
          </a>
          <a href="#services" class="nav-link relative group px-4 py-2 rounded-full transition-all duration-300 hover:bg-white/10">
            A Propos 
            <span class="absolute inset-0 rounded-full bg-gradient-to-r from-blue-400 to-cyan-400 opacity-0 group-hover:opacity-20 transition-opacity"></span>
          </a>
           <a href="#Resume" class="nav-link relative group px-4 py-2 rounded-full transition-all duration-300 hover:bg-white/10">
            Resume 
            <span class="absolute inset-0 rounded-full bg-gradient-to-r from-blue-400 to-cyan-400 opacity-0 group-hover:opacity-20 transition-opacity"></span>
          </a>
          <a href="#innovation" class="nav-link relative group px-4 py-2 rounded-full transition-all duration-300 hover:bg-white/10">
            Compétences
            <span class="absolute inset-0 rounded-full bg-gradient-to-r from-green-400 to-blue-400 opacity-0 group-hover:opacity-20 transition-opacity"></span>
          </a>
           <a href="#projets" class="nav-link relative group px-4 py-2 rounded-full transition-all duration-300 hover:bg-white/10">
            Projets
            <span class="absolute inset-0 rounded-full bg-gradient-to-r from-green-400 to-blue-400 opacity-0 group-hover:opacity-20 transition-opacity"></span>
          </a>
          <a href="#contact" class="nav-link relative group px-4 py-2 rounded-full transition-all duration-300 hover:bg-white/10">
           Contact
            <span class="absolute inset-0 rounded-full bg-gradient-to-r from-yellow-400 to-red-400 opacity-0 group-hover:opacity-20 transition-opacity"></span>
          </a>
        </div>
        <div class="lg:hidden">
          <button class="p-2 rounded-full hover:bg-white/10 transition-colors" id="mobileMenuButton">
            <i class="fas fa-bars text-xl"></i>
          </button>
        </div>
      </div>
    </div>
  </nav>

  <!-- Hero Section -->
  <section id="home" class="hero-3d min-h-screen flex items-center justify-center relative overflow-hidden">
    <div class="absolute inset-0" id="hero3d"></div>
    <div class="max-w-7xl mx-auto px-6 relative z-10">
      <div class="text-center">
        <div class="mb-8">
          <h1 class="text-6xl md:text-8xl font-black mb-6 parallax-element">
            <span class="bg-gradient-to-r from-purple-400 via-pink-400 to-cyan-400 bg-clip-text text-transparent text-glow">
              Hey 👋 I am Aminata TRAORE
            </span>
          </h1>
          <div class="text-xl md:text-2xl text-gray-300 max-w-3xl mx-auto mb-8 parallax-element" data-speed="0.5">
            <span class="typing-text">Développeuse Frontend & Backend passionnée.
              Je transforme des idées en expériences digitales</span>
          </div>
        </div>
        
        <div class="flex flex-col sm:flex-row gap-6 justify-center items-center parallax-element" data-speed="0.3">
          <button class="magnetic-button neon-border px-8 py-4 rounded-full text-lg font-semibold bg-gradient-to-r from-purple-600 to-pink-600 hover:from-purple-500 hover:to-pink-500 transform hover:scale-105 transition-all duration-300">
            Telecharger mon CV <i class="fas fa-rocket ml-2"></i>
          </button>
          <button class="magnetic-button glass-morphism px-8 py-4 rounded-full text-lg font-semibold hover:bg-white/20 transform hover:scale-105 transition-all duration-300">
            Contactez-moi<i class="fas fa-vr-cardboard ml-2"></i>
          </button>
        </div>
        
        <!-- Stats Counter -->
        <div class="grid grid-cols-2 md:grid-cols-4 gap-8 mt-16 parallax-element" data-speed="0.2">
          <div class="holographic-card p-6 rounded-xl text-center">
            <div class="text-3xl font-bold text-cyan-400 mb-2" data-counter="100">0+</div>
            <div class="text-sm text-gray-400">AI Models</div>
          </div>
          <div class="holographic-card p-6 rounded-xl text-center">
            <div class="text-3xl font-bold text-purple-400 mb-2" data-counter="50">10+</div>
            <div class="text-sm text-gray-400">Project R</div>
          </div>
          <div class="holographic-card p-6 rounded-xl text-center">
            <div class="text-3xl font-bold text-pink-400 mb-2" data-counter="200">3+</div>
            <div class="text-sm text-gray-400">Clients</div>
          </div>
          <div class="holographic-card p-6 rounded-xl text-center">
            <div class="text-3xl font-bold text-green-400 mb-2" data-counter="99">50%</div>
            <div class="text-sm text-gray-400">Taux de réussite</div>
          </div>
        </div>
      </div>
    </div>
  </section>


  <section class="pt-1 overflow-hidden black dark:bg-gray-800 md:pt-0 sm:pt-16 2xl:pt-16">
    <h1 class="text-5xl font-bold text-center bg-gradient-to-r from-purple-400 via-pink-400 to-cyan-400 bg-clip-text text-transparent text-glow>A propos de moi">A Propos de moi </h1>
    <div class="px-4 mx-auto sm:px-6 lg:px-8 max-w-7xl">
        <div class="grid items-center grid-cols-1 md:grid-cols-2">

            <div>
                <h2 class="text-3xl font-bold leading-tight text-white dark:text-white sm:text-4xl lg:text-5xl"> I
                    am
                    <br class="block sm:hidden" />Aminata TRAORE
                </h2>
                <p class="max-w-lg mt-3 text-xl leading-relaxed text-white dark:text-gray-300 md:mt-8">
                    Passionnée par la création digitale et l'univers du web.
J'aime construire et donner vie à des projets qui allient simplicité et utilité. Motivée et déterminée.

Mon objectif est de créer des plateformes modernes, fluides et centrées sur l'utilisateur, tout en continuant à évoluer et perfectionner ma manière de penser et de concevoir le web.
                </p>

                <!-- <p class="mt-4 text-xl text-gray-600 dark:text-gray-300 md:mt-8">
                    <span class="relative inline-block">
                        <span class="absolute inline-block w-full bottom-0.5 h-2 bg-yellow-300 dark:bg-gray-900"></span>
                    <span class="relative"> Des question ? </span>
                    </span>
                    <br class="block sm:hidden" />ecrivez mon <a href="#" title=""
                        class="transition-all duration-200 text-sky-500 dark:text-sky-400 hover:text-sky-600 dark:hover:text-sky-500 hover:underline">Linkldin</a>
                </p> -->
            </div>

            <div class="relative">
                <img class="absolute inset-x-0 bottom-0 -mb-48 -translate-x-1/2 left-1/2" src="https://cdn.rareblocks.xyz/collection/celebration/images/team/1/blob-shape.svg" alt="" />

                <img class="relative w-full xl:max-w-lg xl:mx-auto 2xl:origin-bottom 2xl:scale-110" src="../../assets/woman.png" alt="" />
            </div>

        </div>
    </div>
</section>

<div>
    <section class="container mx-auto px-4 py-16 md:py-24">
        <h2 class="text-4xl md:text-5xl font-bold text-center dark:text-white mb-20 bg-gradient-to-r from-purple-400 via-pink-400 to-cyan-400 bg-clip-text text-transparent text-glow">Formation</h2>
        <!-- <p class="text-lg text-center text-white dark:text-gray-300 mb-12 max-w-2xl mx-auto">A scroll-through story of key moments that shaped my development career. Watch the cards animate into view as you explore.</p> -->

        <div class="relative">
            <!-- Central Vertical Line -->
            <div class="absolute left-1/2 transform -translate-x-1/2 h-full w-1 bg-blue-200 dark:bg-blue-900/50"></div>

            <!-- Timeline Items Container -->
            <div class="space-y-12 md:space-y-24">
                <!-- Item 1 -->
                <div class="timeline-item flex flex-col md:flex-row items-center">
                    <!-- Left Side Content (Desktop) -->
                    <div class="hidden md:block md:w-1/2 pr-12"></div>

                    <!-- Icon on Central Line -->
                    <div class="absolute left-1/2 transform -translate-x-1/2 z-10">
                        <div class="flex items-center justify-center w-12 h-12 rounded-full bg-blue-500 text-white border-4 border-white dark:border-gray-900 shadow-lg">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z" />
                            </svg>
                        </div>
                    </div>

                    <!-- Right Side Card -->
                    <div class="ml-0 md:ml-12 md:w-1/2">
                        <div class="timeline-card bg-gray-900 dark:bg-gray-800 rounded-2xl shadow-lg p-6 border-l-4 border-blue-500 transform transition-all duration-500 hover:scale-[1.02]">
                            <p class="text-sm font-semibold text-blue-600 dark:text-blue-400">Juin - Décembre 2025</p>
                            <h3 class="text-xl font-bold text-white dark:text-white mt-2">Développement fullstack</h3>
                            <p class="text-white dark:text-white mt-4">We.Code</p>
                            <!-- <div class="mt-4">
                                <img src="https://images.unsplash.com/photo-1542831371-29b0f74f9713?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=500&q=80" alt="Code screenshot" class="rounded-lg shadow-md">
                            </div> -->
                        </div>
                    </div>
                </div>

                <!-- Item 2 (Alternates on Desktop) -->
                <div class="timeline-item flex flex-col md:flex-row items-center">
                    <!-- Left Side Card -->
                    <div class="md:w-1/2 md:pr-12">
                        <div class="timeline-card bg-gray-900 dark:bg-gray-800 rounded-2xl shadow-lg p-6 border-l-4 border-green-500 transform transition-all duration-500 hover:scale-[1.02]">
                            <p class="text-sm font-semibold text-green-600 dark:text-green-400">2023 - À présent</p>
                            <h3 class="text-xl font-bold text-white dark:text-white mt-2">Licence développement d'application et e-service</h3>
                            <p class="text-white dark:text-white mt-4">Université Virtuelle de Côte d'Ivoire</p>
                            <!-- <div class="mt-4 bg-gray-100 dark:bg-gray-700 p-3 rounded-lg">
                                <pre class="text-xs text-gray-800 dark:text-gray-200"><code>function MyComponent() { return &lt;h1&gt;Wow!&lt;/h1&gt;; }</code></pre>
                            </div> -->
                        </div>
                    </div>

                    <!-- Icon on Central Line -->
                    <div class="absolute left-1/2 transform -translate-x-1/2 z-10">
                        <div class="flex items-center justify-center w-12 h-12 rounded-full bg-green-500 text-white border-4 border-white dark:border-gray-900 shadow-lg">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
                            </svg>
                        </div>
                    </div>

                    <!-- Empty Spacer (Right Side for Desktop) -->
                    <div class="hidden md:block md:w-1/2"></div>
                </div>

                <!-- Item 3 (Add more items following the alternating pattern) -->
                <div class="timeline-item flex flex-col md:flex-row items-center">
                    <div class="hidden md:block md:w-1/2 pr-12"></div>
                    <div class="absolute left-1/2 transform -translate-x-1/2 z-10">
                        <div class="flex items-center justify-center w-12 h-12 rounded-full bg-purple-500 text-white border-4 border-white dark:border-gray-900 shadow-lg">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14.752 11.168l-3.197-2.132A1 1 0 0010 9.87v4.263a1 1 0 001.555.832l3.197-2.132a1 1 0 000-1.664z" />
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
                            </svg>
                        </div>
                    </div>
                    <div class="ml-0 md:ml-12 md:w-1/2">
                        <div class="timeline-card bg-gray-900 dark:bg-gray-800 rounded-2xl shadow-lg p-6 border-l-4 border-purple-500 transform transition-all duration-500 hover:scale-[1.02]">
                            <p class="text-sm font-semibold text-purple-600 dark:text-purple-400">2022 - 2023</p>
                            <h3 class="text-xl font-bold text-white dark:text-white mt-2">Baccalauréat D</h3>
                            <p class="text-white dark:text-white mt-4">Lycée Moderne de Port Bouet</p>
                            <!-- <button class="mt-4 bg-purple-100 dark:bg-purple-900/30 text-purple-600 dark:text-purple-300 text-sm font-medium px-4 py-2 rounded-lg hover:bg-purple-200 dark:hover:bg-purple-900/50 transition-colors">View Project →</button> -->
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</div>

<section class="bg-black text-white mt-64 py-5">
  <h1 class="text-5xl font-bold text-center bg-gradient-to-r from-purple-400 via-pink-400 to-cyan-400 bg-clip-text text-transparent text-glow">Compétences</h1>

  <h2 class="text-3xl font-bold text-center pt-20 mb-6">Langages</h2>
  <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6 max-w-6xl mx-auto mb-12 pt-5">
    <div v-for="lang in languages" :key="lang.name" 
         class="flex flex-col items-center p-4 bg-gray-900 text-white rounded-xl shadow-lg transition transform hover:scale-105 hover:shadow-4xl">
      <img :src="lang.icon" :alt="lang.name" class="w-12 h-12 mb-2">
      <span class="font-semibold">{{ lang.name }}</span>
    </div>
  </div>

  <h2 class="text-3xl font-bold text-center  mb-6">Frameworks / Libraries / Base de Données</h2>
  <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6 max-w-6xl mx-auto mb-12 pt-5">
    <div v-for="fw in frameworks" :key="fw.name" 
         class="flex flex-col items-center p-4 bg-gray-900 text-white rounded-xl shadow-lg transition transform hover:scale-105 hover:shadow-2xl">
      <img :src="fw.icon" :alt="fw.name" class="w-12 h-12 mb-2">
      <span class="font-semibold">{{ fw.name }}</span>
    </div>
  </div>

  <h2 class="text-3xl font-bold text-center mb-6">Outils & Systèmes</h2>
  <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-5 gap-6 max-w-6xl mx-auto pt-5">
    <div v-for="tool in tools" :key="tool.name" 
         class="flex flex-col items-center p-4 bg-gray-900 text-white rounded-xl shadow-lg transition transform hover:scale-105 hover:shadow-2xl">
      <img :src="tool.icon" :alt="tool.name" class="w-12 h-12 mb-2">
      <span class="font-semibold">{{ tool.name }}</span>
    </div>
  </div>
</section>

  <section id="work" class="py-20 px-8">
    <div class="container mx-auto">
      <h2 class="text-4xl font-bold mb-12 bg-gradient-to-r from-purple-400 via-pink-400 to-cyan-400 bg-clip-text text-transparent text-glow">Projets<span class=""></span></h2>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- Project 1 -->
        <div class="tilt-effect" data-tilt data-tilt-max="5" data-tilt-glare="true">
          <div class="glass-card rounded-xl overflow-hidden hover:shadow-lg hover:shadow-neon/20 transition-all h-full">
            <img src="../../assets/free.jpeg" 
                 alt="Project 1" 
                 class="w-full h-48 object-cover">
            <div class="p-6">
              <h3 class="text-xl font-bold mb-2">FreeAds</h3>
              <p class="opacity-80 mb-4">Laravel + Tailwind + MySQL</p>
              <div class="flex flex-wrap gap-2 mb-4">
                <span class="px-3 py-1 bg-glass rounded-full text-sm">Laravel</span>
                <span class="px-3 py-1 bg-glass rounded-full text-sm">Tailwind</span>
                <span class="px-3 py-1 bg-glass rounded-full text-sm">MySQL</span>
              </div>
              <a href="#" class="text-red hover:underline">View Project →</a>
            </div>
          </div>
        </div>
        
        <!-- Project 2 -->
        <div class="tilt-effect" data-tilt data-tilt-max="5" data-tilt-glare="true">
          <div class="glass-card rounded-xl overflow-hidden hover:shadow-lg hover:shadow-cyber/20 transition-all h-full">
            <img src="../../assets/1754919239625.jpeg" 
                 alt="Project 2" 
                 class="w-full h-48 object-cover">
            <div class="p-6">
              <h3 class="text-xl font-bold mb-2">E-Commerce Platform</h3>
              <p class="opacity-80 mb-4">React + GraphQL + Stripe</p>
              <div class="flex flex-wrap gap-2 mb-4">
                <span class="px-3 py-1 bg-glass rounded-full text-sm">React</span>
                <span class="px-3 py-1 bg-glass rounded-full text-sm">GraphQL</span>
                <span class="px-3 py-1 bg-glass rounded-full text-sm">MongoDB</span>
              </div>
              <a href="#" class="text-cyber hover:underline">View Project →</a>
            </div>
          </div>
        </div>
        
        <!-- Project 3 -->
        <div class="tilt-effect" data-tilt data-tilt-max="5" data-tilt-glare="true">
          <div class="glass-card rounded-xl overflow-hidden hover:shadow-lg hover:shadow-matrix/20 transition-all h-full">
            <img src="../../assets/dash.png" 
                 alt="Project 3" 
                 class="w-full h-48 object-cover">
            <div class="p-6">
              <h3 class="text-xl font-bold mb-2">Blockchain Explorer</h3>
              <p class="opacity-80 mb-4">Solidity + Web3.js + Ethers</p>
              <div class="flex flex-wrap gap-2 mb-4">
                <span class="px-3 py-1 bg-glass rounded-full text-sm">Blockchain</span>
                <span class="px-3 py-1 bg-glass rounded-full text-sm">Web3</span>
                <span class="px-3 py-1 bg-glass rounded-full text-sm">React</span>
              </div>
              <a href="#" class="text-matrix hover:underline">View Project →</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  
    <footer class="py-12 px-8 bg-dark-glass">
    <div class="container mx-auto text-center">
      <div class="flex justify-center space-x-6 mb-6">
        <a href="#" class="text-gray-400 hover:text-neon transition-colors">
          <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
          </svg>
        </a>
        <a href="#" class="text-gray-400 hover:text-cyber transition-colors">
          <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/>
          </svg>
        </a>
        <a href="#" class="text-gray-400 hover:text-matrix transition-colors">
          <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z"/>
          </svg>
        </a>
      </div>
      <p class="text-gray-500 text-sm">© 2025 Aminata TRAORE. All rights reserved.</p>
    </div>
  </footer>

</body>
</template>
<script>
export default {
  data() {
    return {
      languages: [
        { name: 'HTML: 80 %', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg' },
        { name: 'CSS', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg' },
        { name: 'JavaScript', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg' },
        { name: 'PHP', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg' }
      ],
      frameworks: [
        { name: 'TailwindCSS', icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-original.svg"},
        { name: 'Laravel', icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/laravel/laravel-original.svg" },
        { name: 'Vue.js', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original.svg' },
        { name: 'React.js', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg' },
        { name: 'Next.js', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nextjs/nextjs-original.svg' },
        { name: 'Nest.js', icon: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nestjs/nestjs-original.svg"},
        { name: 'React Native', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg' },
        { name: 'WordPress', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/wordpress/wordpress-plain.svg' },
        { name: 'MySQL', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg' },
        { name: 'MongoDB', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg' },
      ],
      tools: [
        { name: 'GitHub', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg' },
        { name: 'Postman', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postman/postman-original.svg' },
        { name: 'Trello', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/trello/trello-plain.svg' },
        { name: 'Figma', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg' },
        { name: 'Linux', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg' }
      ]
    };
  },
  mounted() {
    // ====== Tout ton JS ici ======

    // Interactive Cursor
    const cursor = document.getElementById('cursor');
    document.addEventListener('mousemove', e => {
      if(cursor) {
        cursor.style.left = e.clientX + 'px';
        cursor.style.top = e.clientY + 'px';
      }
    });

    // Scroll Progress
    window.addEventListener('scroll', () => {
      const scrolled = (window.scrollY / (document.documentElement.scrollHeight - window.innerHeight)) * 100;
      const scrollBar = document.getElementById('scrollProgress');
      if(scrollBar) scrollBar.style.transform = `scaleX(${scrolled / 100})`;
    });

    // Particle system
    setInterval(() => {
      const container = document.getElementById('particleContainer');
      if(container) {
        const particle = document.createElement('div');
        particle.className = 'particle';
        particle.style.left = Math.random() * 100 + '%';
        particle.style.animationDuration = (Math.random()*3+3)+'s';
        particle.style.animationDelay = Math.random()*2+'s';
        container.appendChild(particle);
        setTimeout(()=>particle.remove(),6000);
      }
    },500);

    // Parallax effect
    document.addEventListener('mousemove', e => {
      const mouseX = e.clientX / window.innerWidth;
      const mouseY = e.clientY / window.innerHeight;
      document.querySelectorAll('.parallax-element').forEach(element=>{
        const speed = element.dataset.speed || 1;
        const x = (mouseX-0.5)*speed*50;
        const y = (mouseY-0.5)*speed*50;
        element.style.transform = `translate3d(${x}px, ${y}px, 0)`;
      });
    });

    // Three.js Hero Background
    const scene = new THREE.Scene();
    const camera = new THREE.PerspectiveCamera(75, window.innerWidth/window.innerHeight,0.1,1000);
    const renderer = new THREE.WebGLRenderer({ alpha:true });
    renderer.setSize(window.innerWidth, window.innerHeight);
    const hero3d = document.getElementById('hero3d');
    if(hero3d) hero3d.appendChild(renderer.domElement);

    const geometry = new THREE.IcosahedronGeometry(1,1);
    const material = new THREE.MeshBasicMaterial({ color:0x667eea, wireframe:true, transparent:true, opacity:0.3 });
    const shapes = [];
    for(let i=0;i<20;i++){
      const mesh = new THREE.Mesh(geometry,material);
      mesh.position.x = (Math.random()-0.5)*20;
      mesh.position.y = (Math.random()-0.5)*20;
      mesh.position.z = (Math.random()-0.5)*20;
      mesh.rotation.x = Math.random()*Math.PI;
      mesh.rotation.y = Math.random()*Math.PI;
      scene.add(mesh);
      shapes.push(mesh);
    }
    camera.position.z=10;
    const animate = ()=>{
      requestAnimationFrame(animate);
      shapes.forEach(shape=>{
        shape.rotation.x+=0.005;
        shape.rotation.y+=0.005;
        shape.position.y+=Math.sin(Date.now()*0.001+shape.position.x)*0.002;
      });
      renderer.render(scene,camera);
    };
    animate();
    window.addEventListener('resize', ()=>{
      camera.aspect=window.innerWidth/window.innerHeight;
      camera.updateProjectionMatrix();
      renderer.setSize(window.innerWidth,window.innerHeight);
    });

    // Typing animation
    const texts = [
      "Dufite ubuhanga bwa AI, VR/AR, Blockchain n'ibindi by'ikoranabuhanga bya none",
      "Turimo gutegura ejo hazaza by'ikoranabuhanga",
      "Innovation, Creativity, and Future Technology Combined"
    ];
    let currentText=0, currentChar=0, isDeleting=false;
    const typeWriter=()=>{
      const element = document.querySelector('.typing-text');
      if(!element) return;
      const current = texts[currentText];
      if(isDeleting){
        element.textContent = current.substring(0,currentChar-1);
        currentChar--;
      } else {
        element.textContent = current.substring(0,currentChar+1);
        currentChar++;
      }
      if(!isDeleting && currentChar===current.length) setTimeout(()=>isDeleting=true,2000);
      else if(isDeleting && currentChar===0){
        isDeleting=false;
        currentText=(currentText+1)%texts.length;
      }
      setTimeout(typeWriter,isDeleting?50:100);
    };
    typeWriter();

    // Ici tu peux continuer avec tous les autres scripts (counters, mobile menu, form, navbar, magnetic buttons)
  }
}
</script>
<!-- <script>
    const toggle = document.getElementById('menu-toggle');
    const mobileMenu = document.getElementById('mobile-menu');

    toggle.addEventListener('click', () => {
      mobileMenu.classList.toggle('hidden');
    });
  </script> -->

    <style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
    
    * {
      font-family: 'Inter', sans-serif;
    }
    
    :root {
      --primary-gradient: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
      --secondary-gradient: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
      --accent-gradient: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
      --dark-gradient: linear-gradient(135deg, #2c3e50 0%, #4a6741 100%);
    }
    
    .glass-morphism {
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(20px);
      border: 1px solid rgba(255, 255, 255, 0.2);
      box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
    }
    
    .floating-orb {
      position: absolute;
      border-radius: 50%;
      filter: blur(40px);
      animation: float-orb 8s ease-in-out infinite;
      z-index: -1;
    }
    
    @keyframes float-orb {
      0%, 100% { transform: translate(0, 0) rotate(0deg); }
      25% { transform: translate(30px, -30px) rotate(90deg); }
      50% { transform: translate(-20px, 20px) rotate(180deg); }
      75% { transform: translate(-30px, -10px) rotate(270deg); }
    }
    
    .hero-3d {
      position: relative;
      overflow: hidden;
    }
    
    .parallax-element {
      transform-style: preserve-3d;
      transition: transform 0.1s ease-out;
    }
    
    .magnetic-button {
      transition: all 0.3s cubic-bezier(0.23, 1, 0.320, 1);
      position: relative;
      overflow: hidden;
    }
    
    .magnetic-button::before {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
      transition: left 0.5s;
    }
    
    .magnetic-button:hover::before {
      left: 100%;
    }
    
    .text-glow {
      text-shadow: 0 0 20px rgba(102, 126, 234, 0.5);
    }
    
    .morphing-card {
      transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
      transform-style: preserve-3d;
    }
    
    .morphing-card:hover {
      transform: translateY(-20px) rotateX(5deg) rotateY(5deg);
    }
    
    .progress-ring {
      transform: rotate(-90deg);
      transform-origin: 50% 50%;
    }
    
    .progress-ring-circle {
      stroke-dasharray: 283;
      stroke-dashoffset: 283;
      transition: stroke-dashoffset 2s cubic-bezier(0.4, 0, 0.2, 1);
    }
    
    .loading-dots {
      display: inline-block;
    }
    
    .loading-dots::after {
      content: '';
      animation: dots 2s linear infinite;
    }
    
    @keyframes dots {
      0%, 20% { content: ''; }
      40% { content: '.'; }
      60% { content: '..'; }
      80%, 100% { content: '...'; }
    }
    
    .neon-border {
      position: relative;
      background: rgba(0,0,0,0.1);
      border: 2px solid transparent;
      background-clip: padding-box;
    }
    
    .neon-border::before {
      content: '';
      position: absolute;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      z-index: -1;
      margin: -2px;
      border-radius: inherit;
      background: linear-gradient(45deg, #667eea, #764ba2, #f093fb, #f5576c);
      animation: rotate-border 4s linear infinite;
    }
    
    @keyframes rotate-border {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }
    
    .typing-animation {
      border-right: 2px solid #667eea;
      animation: blink 1s infinite;
    }
    
    @keyframes blink {
      0%, 50% { border-color: transparent; }
      51%, 100% { border-color: #667eea; }
    }
    
    .particle-container {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      overflow: hidden;
      pointer-events: none;
    }
    
    .particle {
      position: absolute;
      width: 4px;
      height: 4px;
      background: radial-gradient(circle, #667eea, transparent);
      border-radius: 50%;
      animation: particle-float 6s linear infinite;
    }
    
    @keyframes particle-float {
      0% {
        transform: translateY(100vh) scale(0);
        opacity: 0;
      }
      10% {
        opacity: 1;
      }
      90% {
        opacity: 1;
      }
      100% {
        transform: translateY(-10vh) scale(1);
        opacity: 0;
      }
    }
    
    .scroll-progress {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      height: 4px;
      background: var(--primary-gradient);
      transform-origin: 0%;
      z-index: 9999;
      transition: transform 0.1s ease;
    }
    
    .interactive-cursor {
      position: fixed;
      width: 20px;
      height: 20px;
      border: 2px solid #667eea;
      border-radius: 50%;
      pointer-events: none;
      z-index: 9999;
      transition: all 0.1s ease;
      mix-blend-mode: difference;
    }
    
    .section-reveal {
      opacity: 0;
      transform: translateY(50px);
      transition: all 0.8s cubic-bezier(0.23, 1, 0.320, 1);
    }
    
    .section-reveal.revealed {
      opacity: 1;
      transform: translateY(0);
    }
    
    .holographic-card {
      position: relative;
      background: linear-gradient(45deg, rgba(255,255,255,0.1), rgba(255,255,255,0.05));
      border: 1px solid rgba(255,255,255,0.2);
      backdrop-filter: blur(20px);
      overflow: hidden;
    }
    
    .holographic-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.1), transparent);
      transition: left 1s;
    }
    
    .holographic-card:hover::before {
      left: 100%;
    }
    
    @media (max-width: 768px) {
      .particle-container { display: none; }
      .floating-orb { display: none; }
    }
    
    .ai-chat-bubble {
      animation: pulse-glow 2s ease-in-out infinite;
    }
    
    @keyframes pulse-glow {
      0%, 100% { box-shadow: 0 0 20px rgba(102, 126, 234, 0.3); }
      50% { box-shadow: 0 0 40px rgba(102, 126, 234, 0.6); }
    }
  </style>
