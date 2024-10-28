<template>
    <v-container fluid class="py-16 bg-grey-darken-4">
      <v-row class="pt-0 justify-center">
        <v-col cols="12">
            <h1 class="text-white text-h3 text-center font-weight-bold">Garanta a Sua <span class="text-yellow-darken-1">Inscrição</span>!</h1>
        </v-col>
    </v-row>
    <v-row class="pt-4 pb-8 justify-center">
        <v-col cols="12" md="5" class="pr-8" :order="mobile ? '1' : '0'">
          <v-card color="black" rounded="xl" border="0" class="pa-4 px-6 text-center">
            <v-icon size="94" icon="mdi-ticket" color="yellow-darken-1" class="pr-1"></v-icon>
            <div class="pt-4 text-grey-lighten-1 text-caption text-uppercase"><span class="text-yellow-darken-1">1º Lote</span> • Por Apenas</div>
            <p class="pt-0 pb-4 text-h1 text-white font-weight-bold">
                <span class="text-h5 text-grey-lighten-1">R$</span>100
            </p>
            <v-btn 
              height="54" 
              class="text-h5 font-weight-black text-uppercase" 
              variant="flat" 
              block
              color="yellow-darken-1"
              target="_blank"
              href="https://outgo.com.br/ii-pium-mistico-encontro-holistico-potiguar"
            >
              Fazer Inscrição
            </v-btn>
            <div class="pt-2 text-grey-lighten-1 text-caption text-uppercase"><v-icon icon="mdi-lock" color="yellow-darken-1" class="pr-1"></v-icon>Compra Segura</div>
            <p class="pt-8 text-h6" style="line-height: 1.3;">Ingresso válido para os dois dias do evento: <span class="text-yellow-darken-1">9 e 10 de novembro</span>.</p>
            <p class="pt-2 pb-4 text-subtitle-1 text-caption font-weight-regular text-grey-lighten-1"><span class="text-yellow-darken-1">Importante:</span> a Feira Mandalar ocorre em paralelo ao II Pium Místico, também no Espaço Mandalar e é gratuita e aberta ao público geral.</p>
          </v-card>
        </v-col>
        <v-col cols="11" md="5" class="">
          <div class="pt-3 text-left">
            <v-img src="@/assets/logo.png" width="350" class=""></v-img>
          </div>
          <p class="pt-3 text-h5 text-white font-weight-regular">Reserve seu lugar no Pium Místico e viva uma experiência transformadora!</p>
          <p class="pt-3 text-grey-lighten-1">Conecte-se com o autoconhecimento, conheça pessoas e terapias holísticas, e participe de atividades culturais.</p>
          <p class="pt-3 text-grey-lighten-1"><span class="text-yellow-darken-1">E lembre-se:</span> o acesso à Feira Mandalar é gratuito e aberto ao público!</p>
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
  