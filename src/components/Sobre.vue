<template>
  <v-container fluid class="py-16 bg-white">
    <v-row class="pt-8 justify-center">
      <v-col cols="11" class="text-left">
        <p 
          class="font-weight-bold text-purple-darken-4" 
          :class="mobile ? 'text-h4' : 'text-h3'"
        >
          <span>O II Pium Místico é um evento dedicado ao autoconhecimento, saúde mental e espiritualidade</span>
        </p>
        <p class="pt-3 text-h6 font-weight-regular">
          O Pium Místico chega com a intenção de reunir ferramentas e experiências transformadoras que auxiliem as pessoas em sua jornada de autoconhecimento e no despertar da consciência.
        </p>
      </v-col>
    </v-row>
    <v-row class="pt-0 pb-8 justify-center">
      <v-col cols="11" md="5" class="">
        <v-img 
          src="@/assets/puja.jpg" 
          alt="Imagem do II Pium Místico"
          class=""
          min-width="100%"
        ></v-img>
      </v-col>
      <v-col cols="11" md="6" class="" :class="mobile ? '' : 'pl-5'">
        <div class="pt-0 text-h6 font-weight-regular">
          <p class="pt-0 text-h5 font-weight-medium text-purple-darken-4">
            Realizado no Espaço Mandalar, em Pium-RN, nos dias 09 e 10 de novembro de 2024, o encontro contará com palestras, vivências e práticas voltadas ao desenvolvimento pessoal e conexão com o bem-estar.
          </p>
          <p class="pt-3 text-h6 font-weight-regular">
            Em um mundo de ritmo acelerado, que muitas vezes nos desconecta de nossa essência, acreditamos na importância de resgatar o equilíbrio entre corpo, mente e espírito.
          </p>
          <h3 class="pt-3 text-h6 font-weight-regular">
            Venha fazer parte desta jornada transformadora, sintonize-se com seu eu interior e descubra práticas que irão revolucionar sua visão sobre si e o mundo ao seu redor.
          </h3>
        </div>
        <div class="pt-9 text-left">
          <v-btn 
            height="72" 
            class="font-weight-medium text-uppercase" 
            :class="mobile ? 'text-h5' : 'text-h4'"
            variant="flat" 
            block
            color="purple-darken-4"
            href="https://outgo.com.br/ii-pium-mistico-encontro-holistico-potiguar"
          >
            <v-icon icon="mdi-arrow-right" color="yellow-darken-1" class="pr-1"></v-icon>
            Quero Participar
            <v-icon icon="mdi-arrow-left" color="yellow-darken-1" class="pl-1"></v-icon>
          </v-btn>
        </div>
        <p class="pt-2 text-subtitle-1 text-center text-black" style="line-height: 1.3;">Reserve já o seu lugar e vivencie momentos de profunda conexão e aprendizado!</p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
import { ref } from 'vue';
import { useDisplay } from 'vuetify';

const { mobile } = useDisplay();

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
