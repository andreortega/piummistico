<template>
  <v-parallax
    :src="mobile ? backgroundImageMobile : backgroundImageDesktop"
    alt="Background Image"
    height="auto"
  >
    <v-container fluid class="hero-section px-0 py-12">
      <v-row class="pb-16 px-8 px-md-16">
        <v-col cols="12" md="6" class="text-white">
          <v-img src="@/assets/logo.png" width="350" class="mb-8"></v-img>
          <v-chip size="large" color="white" class="px-8 text-overline font-weight-bold mb-4">
            <v-icon class="pr-3">mdi-calendar</v-icon> 09 e 10 de novembro
          </v-chip>
          <h1 class="pt-3 text-yellow-darken-1 font-weight-regular" :class="mobile ? 'text-h2' : 'text-h1'">
            II Pium Místico
          </h1>
          <h6 class="pt-3 text-yellow-darken-1 font-weight-regular text-subtitle-2 text-uppercase">
            <span class="text-white">Tema da Edição</span>
          </h6>
          <h2 class="pt-1 text-yellow-darken-1 font-weight-regular" :class="mobile ? 'text-h6' : 'text-h4'">
            <span>Saúde Mental e Autocuidado: Conexões para o Bem-Estar</span>
          </h2>
          <h3 class="pt-8 font-weight-regular text-white" :class="mobile ? 'text-h5' : 'text-h4'">
            <span>Nos dias 9 e 10 de novembro, em Pium-RN, venha conhecer práticas de autoconhecimento e bem-estar que poderão revolucionar a sua visão sobre si.</span>
          </h3>
          <!-- <v-img v-if="mobile" src="@/assets/evento-mobile.jpg" width="100%" class="my-4"></v-img> -->
          <v-btn
            color="yellow-darken-1"
            size="x-large"
            variant="flat"
            class="mt-6"
            :href="'https://outgo.com.br/ii-pium-mistico-encontro-holistico-potiguar'"
            target="_blank"
            block
          >
            <v-icon left class="pr-2">mdi-eye</v-icon>
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
//import backgroundImage from '@/assets/espaco-mandalar-mobile-bg.jpg';
import backgroundImageMobile from '@/assets/cover-bg-mobile.jpg';
import backgroundImageDesktop from '@/assets/cover-bg-desktop.jpg';

// Detect if the view is on mobile
const { mobile } = useDisplay();

// Use import.meta.glob to load images
//const images = import.meta.glob('@/assets/*.jpg');

// Create a reference for the image source
//let imageSrc = mobile ? images['@/src/assets/espaco-mandalar-mobile.jpg'] : images['@/src/assets/espaco-mandalar-desktop.jpg'];

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
    height: auto !important;
    padding-bottom: 20px;
  }

  .v-btn {
    width: 100%;
  }
}
</style>
