<template>
  <nav class="fixed w-full z-50 py-8 bg-black/50 backdrop-blur-md">
    <div class="max-w-7xl mx-auto px-6 flex justify-between items-center relative">
     <!-- Logo -->
<RouterLink
  to="/"
  class="text-2xl font-bold bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent"
>
  🚀 TAAJ
</RouterLink>


      <!-- Desktop Menu -->
      <div class="hidden lg:flex items-center space-x-8">
  <button @click="goToSection('home')" class="nav-link">
    Accueil
  </button>

  <button @click="goToSection('about')" class="nav-link">
    À Propos
  </button>

  <button @click="goToSection('skills')" class="nav-link">
    Compétences
  </button>

  <button @click="goToSection('formations')" class="nav-link">
    Formations
  </button>

  <button @click="goToSection('ex')" class="nav-link">
    Expériences
  </button>

  <button @click="goToSection('projects')" class="nav-link">
    Projets
  </button>

  <button @click="goToSection('contact')" class="nav-link">
    Contact
  </button>
</div>

      <!-- Mobile Toggle -->
      <button @click="isOpen = !isOpen" class="lg:hidden p-2 rounded-full hover:bg-white/10 transition-colors z-50">
        ☰
      </button>
    </div>

    <!-- Mobile Menu -->
    <transition name="slide-fade">
      <div 
        v-if="isOpen" 
        class="lg:hidden mt-4 bg-black/80 backdrop-blur-md rounded-xl p-4 flex flex-col space-y-3 fixed top-20 left-0 right-0 mx-auto max-w-xs z-50 shadow-lg"
      >
        <a href="#home" class="nav-link" @click="isOpen = false">Accueil</a>
        <a href="#about" class="nav-link" @click="isOpen = false">À Propos</a>
        <a href="#skills" class="nav-link" @click="isOpen = false">Compétences</a>
        <a href="#formations" class="nav-link" @click="isOpen = false">Formations</a>
        <a href="#ex" class="nav-link" @click="isOpen = false">Expériences</a>
        <a href="#projects" class="nav-link" @click="isOpen = false">Projets</a>
        <a href="#contact" class="nav-link" @click="isOpen = false">Contact</a>
      </div>
    </transition>
  </nav>
</template>

<script setup>
import { ref } from 'vue';

const isOpen = ref(false);
const goToSection = (section) => {
  if (window.location.pathname !== '/') {
    window.location.href = `/#${section}`
  } else {
    document.getElementById(section)?.scrollIntoView({
      behavior: 'smooth'
    })
  }
}
</script>

<style scoped>
.nav-link {
  color: white;
  padding: 0.5rem 1rem;
  border-radius: 9999px;
  transition: background 0.3s;
}
.nav-link:hover {
  background: rgba(255,255,255,0.1);
}

/* Slide fade animation */
.slide-fade-enter-active, .slide-fade-leave-active {
  transition: all 0.3s ease;
}
.slide-fade-enter-from, .slide-fade-leave-to {
  transform: translateY(-10px);
  opacity: 0;
}
.slide-fade-enter-to, .slide-fade-leave-from {
  transform: translateY(0);
  opacity: 1;
}
</style>
