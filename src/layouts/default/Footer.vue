<template>
  <v-container fluid class="text-center justify-center mx-0" :class="isMdAndUp ? 'px-16' : 'px-8'">
    <v-row>
      <v-col :cols="isMdAndUp ? 4 : 12">
        <v-btn 
          :block="!isMdAndUp"
          size="x-large"
          :class="isMdAndUp ? 'mr-2' : 'mr-0'"
          @click="goTo('#programacao')"
          target="_blank"
          color="purple"
          variant="flat"
        >
          <v-icon size="x-large" icon="mdi-eye" class="pr-2" /> Ver Programação
        </v-btn>
      </v-col>
      <v-col :cols="isMdAndUp ? 4 : 12">
        <v-btn
          :block="!isMdAndUp"
          size="x-large"
          :class="isMdAndUp ? 'mr-2' : 'mr-0'"
          href="https://www.instagram.com/piummistico/"
          target="_blank"
          color="purple"
          variant="outlined"
        >
          <v-icon size="x-large" icon="mdi-instagram" class="pr-2" /> piummistico
        </v-btn>
      </v-col>
      <v-col :cols="isMdAndUp ? 4 : 12">
        <v-btn 
        :block="!isMdAndUp"
          :class="isMdAndUp ? 'mr-2' : 'mr-0'"
          size="x-large"
          href="https://wa.me/+5584999709599?text=Ol%C3%A1,%20L%C3%BAcia,%20estou%20vindo%20do%20site%20e%20gostaria%20de%20saber%20como%20participar%20do%20Pium%20M%C3%ADstico"

          target="_blank"
          color="#25D366"
          variant="outlined"
        >
          <v-icon size="x-large" icon="mdi-whatsapp" class="pr-2" /> (84) 99970-9599
        </v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
import { useDisplay } from 'vuetify';
import { useGoTo } from 'vuetify'

const { xs, mdAndUp } = useDisplay();
const goTo = useGoTo()

const linkProgramacao = "/programacao-pium-mistico";

const isXs = xs.value;
const isMdAndUp = mdAndUp.value;
</script>
