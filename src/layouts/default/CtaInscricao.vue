<template>
    <v-container fluid class="py-16 bg-yellow-darken-1">
      <v-row class="justify-center">
        <v-col cols="12" md="5">
          <h1 class="text-h4 font-weight-bold text-uppercase text-center">Sobre o II Pium Místico</h1>
          <v-img 
            src="@/assets/evento.jpg" 
            alt="Imagem do II Pium Místico"
            class="my-6"
            height="400"
          ></v-img>
        </v-col>
        <v-col cols="12" md="5">
          <div class="pt-6 text-h6 font-weight-regular">
            <p>O II Pium Místico é um evento dedicado ao autoconhecimento, saúde mental e espiritualidade. Realizado no Espaço Mandalar Pium nos dias 09 e 10 de novembro de 2024, o encontro contará com palestras, vivências e práticas voltadas ao desenvolvimento pessoal e conexão com o bem-estar.</p>
            <p class="pt-3">Venha fazer parte desta jornada transformadora, sintonize-se com seu eu interior e descubra um evento que tocará sua alma.</p>
            <p>Reserve já o seu lugar e vivencie momentos de profunda conexão e aprendizado!</p>
          </div>
          <div class="pt-9 text-left">
            <v-btn 
              height="72" 
              class="text-h5" 
              variant="flat" 
              block
              color="purple-darken-4"
              href="https://outgo.com.br/ii-pium-mistico-encontro-holistico-potiguar"
            >
              <v-icon icon="mdi-arrow-right" color="yellow-darken-1" class="pr-1"></v-icon>
              Fazer Inscrição
              <v-icon icon="mdi-arrow-left" color="yellow-darken-1" class="pl-1"></v-icon>
            </v-btn>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  </script>
  
  <style scoped>
  .avatar-bordered {
    border: 3px solid white;
  }
  .v-card {
    margin-bottom: 16px;
    border: 2px solid #ccc;
    color: #fff;
  }
  .card-title {
    line-height: 1.2;
  }
  </style>
  