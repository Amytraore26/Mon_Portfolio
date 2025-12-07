<script>
export default {
  name: "StepperForm",

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
