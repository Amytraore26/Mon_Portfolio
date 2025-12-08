<template>
  <div
    id="contact"
    class="min-h- bg-black text-white p-4 flex flex-col items-center pb-8"
  >
    <div class="w-full max-w-6xl mt-8">
      <h1
        class="text-5xl font-bold text-center bg-gradient-to-r from-blue-400 to-purple-500 text-transparent bg-clip-text mb-20"
      >
    Contactez-moi
      </h1>
      <!-- <p class="text-center text-gray-400 text-xl mb-12">
        Choose your preferred way to reach out
      </p> -->

      <div class="flex flex-col md:flex-row gap-8 w-full">
        <!-- LEFT SECTION -->
        <div class="bg-gray-800 p-8 rounded-3xl shadow-xl w-full md:w-1/2">
          <h2 class="text-2xl font-bold mb-8">Informations</h2>

          <div class="space-y-8">
            <!-- Email -->
            <div class="flex items-center gap-4 group">
              <div class="bg-blue-900 p-4 rounded-xl">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-blue-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/>
                </svg>
              </div>
              <div>
                <p class="text-gray-400">Email</p>
                <p>aminata.traore@epitech.eu</p>
              </div>
            </div>

            <!-- Phone -->
            <div class="flex items-center gap-4 group">
              <div class="bg-green-900 p-4 rounded-xl">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-green-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/>
                </svg>
              </div>
              <div>
                <p class="text-gray-400">Téléphone</p>
                <p>+225 07 09 87 51 41</p>
              </div>
            </div>

            <!-- Location -->
            <div class="flex items-center gap-4 group">
              <div class="bg-red-900 p-4 rounded-xl">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-red-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/>
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"/>
                </svg>
              </div>
              <div>
                <p class="text-gray-400">Localisation</p>
                <p>Abidjan, Côte d'Ivoire</p>
              </div>
            </div>
          </div>
        </div>

        <!-- RIGHT SECTION (FORM) -->
        <div class="bg-gray-800 p-8 rounded-3xl shadow-xl w-full md:w-1/2">
          <!-- Step 1 -->
          <div v-show="step === 1">
            <h2 class="text-2xl font-bold mb-6">Entrez votre nom</h2>
            <input v-model="form.name" type="text" placeholder="Joelliane......" class="w-full p-4 bg-gray-700 rounded-2xl focus:outline-none focus:ring-2 focus:ring-blue-500 text-white"/>
          </div>

          <!-- Step 2 -->
          <div v-show="step === 2">
            <h2 class="text-2xl font-bold mb-6">Entrez votre nom email</h2>
            <input v-model="form.email" type="email" placeholder="joelliane@gmail.com" class="w-full p-4 bg-gray-700 rounded-2xl focus:outline-none focus:ring-2 focus:ring-blue-500 text-white"/>
          </div>

          <!-- Step 3 -->
          <div v-show="step === 3">
            <h2 class="text-2xl font-bold mb-6">Entrez votre numéro</h2>
            <input v-model="form.phone" type="text" maxlength="11" placeholder="07 00 00 00 00" class="w-full p-4 bg-gray-700 rounded-2xl focus:outline-none focus:ring-2 focus:ring-blue-500 text-white"/>
          </div>

          <!-- Step 4 -->
          <div v-show="step === 4">
            <h2 class="text-2xl font-bold mb-6">Entrez votre message</h2>
            <textarea v-model="form.message" rows="4" placeholder="Bonjour........." class="w-full p-4 bg-gray-700 rounded-2xl focus:outline-none focus:ring-2 focus:ring-blue-500 text-white"></textarea>
            <p class="mt-2 text-sm text-gray-500">Caractères: {{ form.message.length }}/1000</p>
          </div>

          <!-- BUTTONS -->
          <div class="flex justify-between mt-8">
            <button v-show="step > 1" @click="step--" class="px-6 py-3 bg-gray-700 hover:bg-gray-600 rounded-xl transition duration-300">Retour</button>
            <button v-show="step < 4" @click="step++" class="px-6 py-3 bg-blue-600 hover:bg-blue-500 rounded-xl transition duration-300 ml-auto">Suivant</button>
            <button v-show="step === 4" @click="sendEmail" class="px-6 py-3 bg-green-600 hover:bg-green-500 rounded-xl transition duration-300 flex items-center gap-2">Envoyer</button>
          </div>

          <!-- STEP INDICATORS -->
          <div class="flex justify-center mt-8 gap-2">
            <div v-for="n in 4" :key="n" :class="['h-2 rounded-full transition-all duration-300', step === n ? 'w-8 bg-blue-500' : 'w-2 bg-gray-600']"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import emailjs from 'emailjs-com';

export default {
  name: "Contact",
  data() {
    return {
      step: 1,
      form: {
        name: "",
        email: "",
        phone: "",
        message: "",
      },
    };
  },
  methods: {
    sendEmail() {
      const templateParams = {
        from_name: this.form.name,
        from_email: this.form.email,
        phone: this.form.phone,
        message: this.form.message,
      };

      emailjs.send('service_38knslv', 'template_gh8m972', templateParams, 'MCDNanu_vhZFoeaSk')
        .then(() => {
          alert('Message envoyé avec succès !');
          this.step = 1;
          this.form = { name: "", email: "", phone: "", message: "" };
        }, (error) => {
          console.error(error);
          alert('Erreur lors de l\'envoi.');
        });
    }
  }
}
</script>
