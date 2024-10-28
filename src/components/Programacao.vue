<template>
  <v-container id="programacao" class="pt-16 pb-16">
    <v-row class="pt-16 pb-8 justify-center">
      <v-col cols="11" class="pb-8 text-center">
        <h1 class="text-h3 text-white">Programação do Evento</h1>
        <h2 class="pt-3 text-h6 text-white font-weight-regular" style="line-height: 1.3;">Confira as atividades e palestras dos dias <span class="text-yellow-darken-1">09 e 10 de novembro</span></h2>
      </v-col>
      <!-- Coluna Sábado -->
      <v-col cols="11" md="6">
        <div class="pb-4 text-center">
          <v-icon size="24" color="purple-lighten-3">mdi-arrow-down</v-icon>
          <span class="text-yellow-darken-1 text-h6 font-weight-medium pr-1"> SÁBADO <span class="text-white">•</span> 09.NOV</span>
          <v-icon size="24" color="purple-lighten-3">mdi-arrow-down</v-icon>
        </div>
        <v-card
          v-for="(atividade, index) in programacao[0]" :key="index"
          class="elevation-2"
          color="transparent"
          rounded="lg"
          outlined
          style="border: 2px solid #ccc; margin-bottom: 16px; color: #fff;"
        >
          <v-row>
            <v-col>
              <v-chip size="sm" class="mt-3 mx-2 px-3 " color="yellow-darken-1" text-color="white">{{ atividade.horario }}</v-chip>
              <v-card-title class="pt-2 pb-0 text-white text-h5" style="white-space: normal;">
                {{ atividade.titulo }}
              </v-card-title>
              <v-card-subtitle class="pt-1 text-purple-lighten-5 text-uppercase" style="white-space: normal;">
                {{ atividade.subtitulo }}
              </v-card-subtitle>
            </v-col>
          </v-row>
          <v-row>
            <v-col cols="3" md="2"class="pl-7">
              <v-avatar
                v-if="atividade.imagem"
                class="avatar-bordered"
                size="72"
                :image="atividade.imagem"
              ></v-avatar>
            </v-col>
            <v-col cols="7" md="10" class="pl-4">
              <div v-if="atividade.convidado" class="text-h6 text-yellow-darken-1">{{ atividade.convidado }}<br></div>
              <div v-if="atividade.minicurriculo" class="text-subtitle-1 text-purple-lighten-5 font-weight-light" style="line-height: 1.3;">{{ atividade.minicurriculo }}<br></div>
            </v-col>
          </v-row>
          <v-card-text class="text-white" style="font-size: 1.1em;">
            {{ atividade.descricao }}
          </v-card-text>
          <v-card-actions>
            <v-btn text color="yellow-darken-1" @click="atividade.expanded = !atividade.expanded">
              {{ atividade.expanded ? 'Ver Menos' : 'Ver Mais' }}
            </v-btn>
          </v-card-actions>
          <v-expand-transition>
            <v-card-text v-if="atividade.expanded" class="text-white">
              <strong>Sobre {{ atividade.convidado }}</strong><br>
              {{ atividade.sobreConvidado }}
              <br><br>
              <strong>Sobre a Atividade</strong><br>
              {{ atividade.sobreAtividade }}
            </v-card-text>
          </v-expand-transition>
        </v-card>
      </v-col>
      <!-- Coluna Domingo -->
      <v-col cols="11" md="6">
        <div class="pb-4 text-center">
          <v-icon size="24" color="purple-lighten-3">mdi-arrow-down</v-icon>
          <span class="text-yellow-darken-1 text-h6 font-weight-medium pr-1"> DOMINGO <span class="text-white">•</span> 10.NOV</span>
          <v-icon size="24" color="purple-lighten-3">mdi-arrow-down</v-icon>
        </div>
        <v-card
          v-for="(atividade, index) in programacao[1]" :key="index"
          class="elevation-2"
          color="transparent"
          rounded="lg"
          outlined
          style="border: 2px solid #ccc; margin-bottom: 16px; color: #fff;"
        >
          <v-row>
            <v-col>
              <v-chip size="sm" class="mt-3 mx-2 px-3 " color="yellow-darken-1" text-color="white">{{ atividade.horario }}</v-chip>
              <v-card-title class="pt-2 pb-0 text-white text-h5" style="white-space: normal;">
                {{ atividade.titulo }}
              </v-card-title>
              <v-card-subtitle class="pt-1 text-purple-lighten-5 text-uppercase" style="white-space: normal;">
                {{ atividade.subtitulo }}
              </v-card-subtitle>
            </v-col>
          </v-row>
          <v-row>
            <v-col cols="3" md="2"class="pl-7">
              <v-avatar
                v-if="atividade.imagem"
                class="avatar-bordered"
                size="72"
                :image="atividade.imagem"
              ></v-avatar>
            </v-col>
            <v-col cols="7" md="10" class="pl-4">
              <div v-if="atividade.convidado" class="text-h6 text-yellow-darken-1">{{ atividade.convidado }}<br></div>
              <div v-if="atividade.minicurriculo" class="text-subtitle-1 text-purple-lighten-5 font-weight-light" style="line-height: 1.3;">{{ atividade.minicurriculo }}<br></div>
            </v-col>
          </v-row>
          <v-card-text class="text-white" style="font-size: 1.1em;">
            {{ atividade.descricao }}
          </v-card-text>
          <v-card-actions>
            <v-btn text color="yellow-darken-1" @click="atividade.expanded = !atividade.expanded">
              {{ atividade.expanded ? 'Ver Menos' : 'Ver Mais' }}
            </v-btn>
          </v-card-actions>
          <v-expand-transition>
            <v-card-text v-if="atividade.expanded" class="text-white">
              <strong>Sobre {{ atividade.convidado }}</strong><br>
              {{ atividade.sobreConvidado }}
              <br><br>
              <strong>Sobre a Atividade</strong><br>
              {{ atividade.sobreAtividade }}
            </v-card-text>
          </v-expand-transition>
        </v-card>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" class="pb-16">
        <div class="text-left">
          <v-btn 
            height="72" 
            class="text-h4 font-weight-medium text-uppercase" 
            variant="flat" 
            block
            color="yellow-darken-1"
            target="_blank"
            href="https://outgo.com.br/ii-pium-mistico-encontro-holistico-potiguar"
          >
            <v-icon icon="mdi-arrow-right" color="purple-darken-3" class="pr-1"></v-icon>
            Fazer Inscrição
            <v-icon icon="mdi-arrow-left" color="purple-darken-3" class="pl-1"></v-icon>
          </v-btn>
        </div>
        <p class="pt-1 font-weight-light text-subtitle-1 text-center text-white">Reserve já o seu lugar e vivencie momentos de profunda conexão e aprendizado!</p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const programacao = ref([]);

onMounted(async () => {
  try {
    const response = await fetch('./programacao.json');
    const data = await response.json();

    // Verificando se o JSON é um array com duas posições
    if (Array.isArray(data) && data.length === 2) {
      programacao.value = data.map((dia) => {
        return dia.map((atividade) => ({
          ...atividade,
          expanded: false // Inicializa o estado 'expanded' para cada atividade
        }));
      });
      console.log('Dados da programação carregados:', programacao.value);
    } else {
      console.error('Estrutura do JSON inválida. Esperava um array com duas posições (sábado e domingo).');
    }
  } catch (error) {
    console.error('Erro ao carregar a programação:', error);
  }
});
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
.v-card-title {
  line-height: 1.2 !important;
  font-size: 1.4em;
}
</style>
