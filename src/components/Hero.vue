<template>
  <v-parallax
    src="@/assets/espaco-mandalar.jpg"
    height="100vh"
    alt="Background Image"
  >
    <v-container fluid class="hero-section px-0">
      <v-row class="fill-height d-flex align-start justify-start px-md-10 px-4">
        <v-col cols="12" md="6" class="d-flex flex-column align-start px-md-10 px-4 text-white">
          <v-img src="@/assets/logo.png" width="350" class="mb-8"></v-img>
          <v-chip size="large" color="white" class="px-5 text-overline font-weight-bold mb-4">
            <v-icon class="pr-3">mdi-calendar</v-icon> 09 e 10 de novembro
          </v-chip>
          <h1 class="pt-3 text-h2 text-yellow-darken-1">II Pium Místico: Saúde Mental e Autoconhecimento</h1>
          <h3 class="pt-3 text-h6 font-weight-regular text-yellow">
            Um movimento de despertar, bem-estar e conexão com o ser, oferecendo práticas transformadoras para promover equilíbrio e autodescoberta em um ambiente acolhedor e inspirador.
          </h3>
          <v-img v-if="mobile" src="@/assets/puja.jpg" width="100%" class="my-4"></v-img>
          <h3 class="pt-3 text-h6 font-weight-regular text-white">
            Participe do Pium Místico e descubra práticas que promovem o equilíbrio emocional, bem-estar e uma conexão profunda consigo mesmo. Aprenda com palestrantes renomados, participe de vivências práticas e inspire-se em um ambiente criado para a transformação pessoal.
          </h3>
          <v-btn
            color="yellow-darken-1"
            size="x-large"
            variant="flat"
            class="mt-6 mb-16"
            :href="'https://outgo.com.br/ii-pium-mistico-encontro-holistico-potiguar'"
            target="_blank"
            block
          >
            <v-icon left>mdi-eye</v-icon>
            Fazer Inscrição Agora
          </v-btn>
        </v-col>
      </v-row>
    </v-container>
  </v-parallax>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import axios from 'axios';
import { useDisplay } from 'vuetify';

// Detect if the view is on mobile
const { mobile } = useDisplay();

// Function to scroll to the registration section
const scrollToRegistration = () => {
  const registrationElement = document.getElementById('registration-section');
  if (registrationElement) {
    registrationElement.scrollIntoView({ behavior: 'smooth' });
  }
};
</script>

<style scoped>
.hero-section {
  position: relative;
}

.fill-height {
  height: 100vh;
}

.text-yellow {
  color: #FFD700 !important;
}

.text-white {
  color: #ffffff !important;
}

@media (max-width: 960px) {
  .px-md-10 {
    padding-left: 16px;
    padding-right: 16px;
  }
}

@media (max-width: 600px) {
  .fill-height {
    height: auto;
    padding-bottom: 20px;
  }

  .v-btn {
    width: 100%;
  }
}
</style>
