<template>
<v-app>
  <!-- <default-bar /> -->
  <v-main>
    <v-container fluid fill-height class="fill-height px-0 mx-0 py-0 my-0">
      <v-row class="align-center justify-center">
        <v-col cols="12">
          <iframe :src="'https://piumistico.com.br/programacao-pium-mistico.pdf'" width="100%" style="height: 100vh !important" frameborder="0"></iframe>
        </v-col>
      </v-row>
    </v-container>
  </v-main>
</v-app>
</template>

<script setup>
import { ref, onMounted } from 'vue';
//simport DefaultBar from './AppBar.vue'
//import axios from 'axios';

const pdfsrc = ref(null);

const getPDFPath = () => {
  // axios
  //   .get('/pium-mistico.pdf', {
  //     responseType: 'blob'
  //   })
  //   .then(response => {
  //     console.log('Success', response);
  //     const blob = new Blob([response.data]);
  //     const objectUrl = URL.createObjectURL(blob);
  //     pdfsrc.value = objectUrl;
  //   })
  //   .catch(console.error);
  // const pdfPath = '/pium-mistico.pdf'; // Caminho relativo à pasta 'public'
  // const objectUrl = new URL(pdfPath, import.meta.env.BASE_URL).href;
  // pdfsrc.value = objectUrl;
};

onMounted(() => {
  getPDFPath();
});
</script>