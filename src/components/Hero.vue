<template>
  <v-container fluid class="hero-section px-0">
    <v-img
      src="@/assets/espaco-mandalar.jpg"
      height="100vh"
      class="background-img"
      gradient="to bottom, rgba(0,0,0,.5), rgba(0,0,0,.2)"
    >
      <v-row class="fill-height d-flex align-center justify-center">

        <v-col cols="12" md="6" class="d-flex justify-center">
          <v-img :src="'/@/assets/destaque.jpg'" aspect-ratio="4/5" class="highlight-img"></v-img>
        </v-col>

        <v-col cols="12" md="6" class="d-flex flex-column align-start px-10">
          <v-img src="@/assets/logo.png" contain max-width="200" class="mb-5"></v-img>
          <h1 class="display-3 white--text mb-3">II Pium Místico: Saúde Mental e Autoconhecimento</h1>
          <h2 class="subtitle-1 white--text mb-5">
            Um movimento de despertar, bem-estar e conexão com o ser, oferecendo práticas transformadoras para promover equilíbrio e autodescoberta em um ambiente acolhedor e inspirador
          </h2>
          <p class="white--text mb-5">
            Participe do Pium Místico e descubra práticas que promovem o equilíbrio emocional, bem-estar e uma conexão profunda consigo mesmo. Aprenda com palestrantes renomados, participe de vivências práticas e inspire-se em um ambiente criado para a transformação pessoal.
          </p>
          <v-btn class="mb-5" color="primary" @click="scrollToRegistration">
            Inscreva-se Agora
          </v-btn>
          <v-row>
            <v-col cols="4">
              <v-img :src="'/@/assets/pequena-imagem1.jpg'" max-width="100"></v-img>
            </v-col>
            <v-col cols="4">
              <v-img :src="'/@/assets/pequena-imagem2.jpg'" max-width="100"></v-img>
            </v-col>
            <v-col cols="4">
              <v-img :src="'/@/assets/pequena-imagem3.jpg'" max-width="100"></v-img>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-img>
  </v-container>
</template>

<script setup>
import { ref } from 'vue';

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

.background-img {
  width: 100%;
  height: 100vh;
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
}

.text-overlay {
  text-align: left;
}

.v-btn {
  background-color: #ff4081 !important;
  color: #ffffff !important;
}

.fill-height {
  height: 100vh;
}

.highlight-img {
  max-width: 400px;
  border-radius: 8px;
}
</style>

