<template>
  <v-container fluid class="py-16 bg-yellow-lighten-5">
    <v-row class="pt-8 justify-center">
      <v-col cols="11" class="text-center">
        <v-img 
          src="@/assets/logo-feira.png" 
          alt="Logo da Feira Mandalar"
          class="pt-8 mx-auto"
          width="180"
        ></v-img>
        <v-chip size="large" color="purple-darken-4" class="px-8 text-overline font-weight-bold mb-4">
          <v-icon class="pr-3">mdi-gift</v-icon> Atividade Extra • Aberto ao Público
        </v-chip>
        <p class="font-weight-medium text-purple-darken-4" :class="mobile ? 'text-h5' : 'text-h3'">
          Feira Mandalar
        </p>
        <p class="pt-4 text-h5">Evento GRATUITO e aberto ao público, também acontecerá nos dias 9 e 10 de novembro, das 9h às 18h, em paralelo ao Pium Místico, no Espaço Mandalar, em Pium.</p>
      </v-col>
    </v-row>
    <v-row class="pt-0 justify-center">
      <!-- <v-col cols="12" md="5">
        <div class="pt-0 text-h6 font-weight-regular">
          <p class="pt-0 font-weight-medium">Realizado no Espaço Mandalar Pium nos dias 09 e 10 de novembro de 2024, o encontro contará com palestras, vivências e práticas voltadas ao desenvolvimento pessoal e conexão com o bem-estar.</p>
          <p class="pt-3 text-subtitle-1">Venha fazer parte desta jornada transformadora, sintonize-se com seu eu interior e descubra um evento que tocará sua alma.</p>
          <h3 class="pt-3 text-subtitle-1 font-weight-regular">
            Garanta a sua vaga neste evento que acontecerá no Espaço Mandalar! Participe de vivências, conheça especialistas em saúde mental e mergulhe em uma jornada de autodescoberta.
          </h3>
        </div>
      </v-col> -->
      <v-col cols="11" class="pr-8 ">
        <v-img 
          src="@/assets/feira.jpg" 
          alt="Imagem da Feira Mandalar"
          class=""
          width="100%"
        ></v-img>
      </v-col>
      <v-col cols="11" class="pb-16 text-center">
        <p class="font-weight-medium text-purple-darken-4 text-uppercase" :class="mobile ? 'text-h5' : 'text-h5'">
          Acesso Gratuito!
        </p>
        <p class="pt-2 text-subtitle-1 ">Com atividades interativas, workshops, terapias holísticas, artesanato e apresentações culturais, é o lugar perfeito para quem busca conexão, bem-estar e espiritualidade em meio à natureza.</p>
        <p class="pt-3 text-subtitle-1 text-purple-darken-4 font-weight-medium text-uppercase">Só vem! <v-icon color="purple-darken-4">mdi-emoticon-wink-outline</v-icon></p>
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
