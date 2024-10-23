<template>
  <div class="hero-section pt-0">
    <v-container fluid class="px-0 pt-0 mt-0">
      <v-row class="fill-height d-flex align-center justify-center px-16">
        <v-col cols="12" md="6" class="align-start px-16 pb-16 mb-16 text-white">
          <v-img src="@/assets/logo.png" contain max-width="350" class="mb-8"></v-img>
          <v-chip size="large" color="white" class="px-5 text-overline font-weight-bold">
            <v-icon class="pr-3">mdi-calendar</v-icon> 09 e 10 de novembro
          </v-chip>
          <h1 class="pt-3 text-h2 text-yellow-darken-1">II Pium Místico: Saúde Mental e Autoconhecimento</h1>
          <h3 class="pt-3 text-h6 font-weight-regular">
            Um movimento de despertar, bem-estar e conexão com o ser, oferecendo práticas transformadoras para promover equilíbrio e autodescoberta em um ambiente acolhedor e inspirador
          </h3>
          <h3 class="pt-3 text-h6 font-weight-regular">
            Participe do Pium Místico e descubra práticas que promovem o equilíbrio emocional, bem-estar e uma conexão profunda consigo mesmo. Aprenda com palestrantes renomados, participe de vivências práticas e inspire-se em um ambiente criado para a transformação pessoal.
          </h3>
          <!-- <h3 class="pt-9 text-h4 font-weight-regular text-yellow-darken-1">Tema Central: A Integração do Ser e a Relação com o Planeta</h3>
          <h3 class="pt-3 text-h6 font-weight-regular">
            Explore a fascinante interligação entre o ser humano e o planeta em que vivemos. Nossos palestrantes, terapeutas e cientistas renomados irão conduzir discussões envolventes sobre como a harmonia entre nosso ser interior e a natureza ao nosso redor é fundamental para uma vida equilibrada e saudável.
          </h3>
          <h3 class="pt-9 text-h4 font-weight-regular text-yellow-darken-1">O Que Esperar</h3>
          <h3 class="pt-3 text-h6 font-weight-regular"><span class="text-yellow-darken-1">Palestras Inspiradoras:</span> Ouça vozes influentes do mundo holístico e científico compartilhando suas perspectivas sobre autoconhecimento, saúde integral e sustentabilidade.</h3>
          <h3 class="pt-3 text-h6 font-weight-regular"><span class="text-yellow-darken-1">Vivências Transformadoras:</span> Participe de práticas terapêuticas, meditações guiadas, danças sagradas e outras vivências que irão expandir sua consciência.</h3>
          <h3 class="pt-3 text-h6 font-weight-regular"><span class="text-yellow-darken-1">Feira de Gastronomia e Artesanato:</span> Delicie-se com opções saudáveis e saborosas enquanto explora criações artesanais inspiradoras.</h3>
          <h3 class="pt-3 text-h6 font-weight-regular"><span class="text-yellow-darken-1">Conexões Profundas:</span> Conheça pessoas afins e crie laços duradouros com uma comunidade unida pelo desejo de evolução e cura.</h3> -->
          <!-- <v-btn class="mb-5 mt-4" color="yellow-darken-1" @click="scrollToRegistration">
            Inscreva-se Agora
          </v-btn> -->
          <v-btn
            color="yellow-darken-1"
            :to="linkProgramacao"
            size="x-large"
            target="_blank"
            variant="flat"
            class="mt-6 mb-16"
            block
          >
            <v-icon icon="mdi-eye" size="large" start />
            Fazer Inscrição Agora
          </v-btn>
          <!-- <v-row>
            <v-col cols="4">
              <v-img :src="'/@/assets/pequena-imagem1.jpg'" max-width="100"></v-img>
            </v-col>
            <v-col cols="4">
              <v-img :src="'/@/assets/pequena-imagem2.jpg'" max-width="100"></v-img>
            </v-col>
            <v-col cols="4">
              <v-img :src="'/@/assets/pequena-imagem3.jpg'" max-width="100"></v-img>
            </v-col>
          </v-row> -->
        </v-col>

        <v-col cols="12" md="6" class="">
          <!-- <v-img src="@/assets/espaco-mandalar.jpg" aspect-ratio="4/5" class="highlight-img"></v-img> -->
          
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script setup>
import { computed } from 'vue';

const linkProgramacao = "/programacao-pium-mistico";

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
  background-image: url('@/assets/espaco-mandalar.jpg');
  background-size: cover;
  background-position: center;
  width: 100%;
  height: 100vh;
  display: flex;
  align-items: start;
  justify-content: start;
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