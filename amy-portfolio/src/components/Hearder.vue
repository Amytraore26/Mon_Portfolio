<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div>
<body class="bg-gray-100">

  <nav class="bg-gradient-to-r from-indigo-600 via-purple-600 to-pink-500 shadow-lg">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between h-16 items-center">
        <!-- Logo -->
        <div class="flex-shrink-0 text-white text-2xl font-bold">
          MyBrand
        </div>

        <!-- Desktop Menu -->
        <div class="hidden md:flex space-x-6 text-white font-medium">
          <a href="#" class="hover:text-yellow-300 transition">Home</a>
          <a href="#" class="hover:text-yellow-300 transition">About</a>
          <a href="#" class="hover:text-yellow-300 transition">Services</a>
          <a href="#" class="hover:text-yellow-300 transition">Contact</a>
        </div>

        <!-- Desktop Button -->
        <div class="hidden md:block">
          <a href="#" class="bg-white text-indigo-700 px-4 py-2 rounded-xl hover:bg-yellow-300 transition-all font-semibold">
            Get Started
          </a>
        </div>

        <!-- Mobile Menu Button -->
        <div class="md:hidden">
          <button id="menu-toggle" class="text-white focus:outline-none text-2xl">
            ☰
          </button>
        </div>
      </div>
    </div>

    <!-- Mobile Menu -->
    <div id="mobile-menu" class="md:hidden hidden px-4 pb-4 space-y-2 text-white font-medium">
      <a href="#" class="block hover:text-yellow-300 transition">Home</a>
      <a href="#" class="block hover:text-yellow-300 transition">About</a>
      <a href="#" class="block hover:text-yellow-300 transition">Services</a>
      <a href="#" class="block hover:text-yellow-300 transition">Contact</a>
      <a href="#" class="block bg-white text-indigo-700 text-center px-4 py-2 rounded-xl hover:bg-yellow-300 transition-all font-semibold mt-2">
        Get Started
      </a>
    </div>
  </nav>
</body>
</div>
<body class="bg-gray-50">
    <!-- Hero Section -->
    <section class="relative bg-gradient-to-br from-purple-900 via-indigo-800 to-blue-900 text-white overflow-hidden">
        <div class="absolute inset-0 opacity-10">
            <div class="absolute top-0 left-0 w-full h-full bg-[url('https://grainy-gradients.vercel.app/noise.svg')]"></div>
        </div>
        
        <div class="container mx-auto px-6 py-24 relative z-10">
            <div class="flex flex-col lg:flex-row items-center">
                <div class="lg:w-1/2 mb-12 lg:mb-0">
                    <h1 class="text-4xl md:text-6xl font-bold mb-6 leading-tight">
                        Build Amazing <span class="gradient-text bg-gradient-to-r from-pink-500 to-yellow-500">Digital Experiences</span>
                    </h1>
                    <p class="text-xl text-blue-100 mb-8 max-w-lg">
                        Our platform helps you create stunning websites and applications with minimal effort and maximum creativity.
                    </p>
                    <div class="flex flex-col sm:flex-row space-y-4 sm:space-y-0 sm:space-x-4">
                        <button class="bg-gradient-to-r from-pink-500 to-yellow-500 text-white px-8 py-4 rounded-xl font-bold hover:from-pink-600 hover:to-yellow-600 transition-all transform hover:scale-105 shadow-lg">
                            Get Started Free
                        </button>
                        <button class="bg-white bg-opacity-20 text-white px-8 py-4 rounded-xl font-bold hover:bg-opacity-30 transition-all border border-white border-opacity-30">
                            Learn More
                        </button>
                    </div>
                </div>
                <div class="lg:w-1/2 flex justify-center">
                    <div class="relative w-full max-w-md">
                        <div class="absolute -top-10 -left-10 w-32 h-32 bg-pink-500 rounded-full filter blur-3xl opacity-30"></div>
                        <div class="absolute -bottom-10 -right-10 w-32 h-32 bg-blue-500 rounded-full filter blur-3xl opacity-30"></div>
                        <img src="../router/i.jpeg" 
                             alt="Hero Image" 
                             class="relative z-10 w-full floating">
                    </div>
                </div>
            </div>
        </div>
        <div class="absolute bottom-0 left-0 right-0 h-32 bg-gradient-to-t from-gray-50 to-transparent"></div>
    </section>

    <div class="font font-Poppins bg-gray-100 min-h-screen">
  <div class="flex flex-col items-center relative pt-20 overflow-hidden">
    <!-- Animated Background Text -->
    <h1 class="absolute text-6xl md:text-[10rem] font-bold text-black-100 opacity-1 animate-pulse">
      ABOUT ME
    </h1>
    
    <div class="relative flex flex-col items-center mt-5 md:mt-10 group">
      <!-- Main Heading with Gradient Text -->
      <h1 class="text-3xl md:text-5xl lg:text-7xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-orange-500 to-amber-300 mb-2 transition-all duration-500 group-hover:scale-105">
        Know Me More
      </h1>
      
      <!-- Animated Border -->
      <div class="relative">
        <div class="w-20 md:w-32 h-1 bg-gray-600 rounded-full overflow-hidden">
          <div class="h-full bg-orange-600 animate-progress-bar origin-left"></div>
        </div>
        <div class="absolute -bottom-1 left-1/2 transform -translate-x-1/2 w-2 h-2 bg-orange-400 rounded-full animate-ping"></div>
      </div>
      
      <!-- Subtle decorative elements -->
     
    </div>
    
    <!-- Optional subtitle -->
    <p class="mt-6 text-gray-400 text-center max-w-md md:max-w-2xl px-4 text-sm md:text-base animate-fade-in">
      Let me introduce myself and share my journey, skills, and passions with you      Let me introduce myself and share my journey, skills, and passions with you

            Let me introduce myself and share my journey, skills, and passions with you


    </p>
  </div>
</div>

    <section class="py-12 bg-gray-100">

    <h2 class="text-3xl font-bold text-center mb-6">Langages</h2>
    <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-5 gap-6 max-w-6xl mx-auto mb-12">
      <div v-for="lang in languages" :key="lang.name" class="flex flex-col items-center p-4 bg-white rounded-xl shadow-lg transition transform hover:scale-105 hover:shadow-2xl">
        <img :src="lang.icon" :alt="lang.name" class="w-12 h-12 mb-2">
        <span class="text-gray-700 font-semibold">{{ lang.name }}</span>
      </div>
    </div>

    <h2 class="text-3xl font-bold text-center mb-6">Frameworks / Libraries</h2>
    <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-5 gap-6 max-w-6xl mx-auto mb-12">
      <div v-for="fw in frameworks" :key="fw.name" class="flex flex-col items-center p-4 bg-white rounded-xl shadow-lg transition transform hover:scale-105 hover:shadow-2xl">
        <img :src="fw.icon" :alt="fw.name" class="w-12 h-12 mb-2">
        <span class="text-gray-700 font-semibold">{{ fw.name }}</span>
      </div>
    </div>

    <h2 class="text-3xl font-bold text-center mb-6">Outils & Systèmes</h2>
    <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-5 gap-6 max-w-6xl mx-auto">
      <div v-for="tool in tools" :key="tool.name" class="flex flex-col items-center p-4 bg-white rounded-xl shadow-lg transition transform hover:scale-105 hover:shadow-2xl">
        <img :src="tool.icon" :alt="tool.name" class="w-12 h-12 mb-2">
        <span class="text-gray-700 font-semibold">{{ tool.name }}</span>
      </div>
    </div>

  </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-400 py-12">
        <div class="container mx-auto px-6">
            <div class="border-t border-gray-800 mt-12 pt-8 flex flex-col md:flex-row justify-between items-center">
                <div class="mb-4 md:mb-0">
                    <a href="#" class="text-white text-2xl font-bold flex items-center">
                        <i class="fas fa-crown text-yellow-500 mr-2"></i> BrandName
                    </a>
                </div>
                <div class="text-sm">
                    &copy; 2023 BrandName. All rights reserved.
                </div>
            </div>
        </div>
    </footer>

</body>
</template>

<script>
export default {
  data() {
    return {
      languages: [
        { name: 'HTML', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg' },
        { name: 'CSS', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg' },
        { name: 'JavaScript', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg' },
        { name: 'PHP', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg' }
      ],

      frameworks: [
        { name: 'Vue.js', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original.svg' },
        { name: 'React.js', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg' },
        { name: 'React Native', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg' },
        { name: 'Next.js', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nextjs/nextjs-original.svg' },
        { name: 'Laravel', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/laravel/laravel-plain.svg' },
        { name: 'WordPress', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/wordpress/wordpress-plain.svg' }
      ],

      tools: [
        { name: 'Postman', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postman/postman-original.svg' },
        { name: 'VS Code', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg' },
        { name: 'Trello', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/trello/trello-plain.svg' },
        { name: 'Figma', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg' },
        { name: 'Photoshop', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/photoshop/photoshop-plain.svg' },
        { name: 'Git', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg' },
        { name: 'GitHub', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg' },
        { name: 'Linux', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg' }
      ]
    }
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
