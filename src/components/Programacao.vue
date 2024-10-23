<template>
  <v-container class="pt-16 pb-16">
    <v-row class="pb-16">
      <v-col cols="12" class="pb-8 text-center">
        <v-card-title class="text-h4 text-white">Programação</v-card-title>
        <v-card-subtitle class="text-h6 text-white">Confira as atividades e palestras dos dias 09 e 10 de novembro</v-card-subtitle>
      </v-col>
      <!-- Coluna Sábado -->
      <v-col cols="12" md="6">
        <div class="pb-2">
          <span class="text-white text-h6">SÁBADO • 09.NOV</span>
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
            <v-col cols="2" class="pl-6">
              <v-avatar
                v-if="atividade.imagem"
                class="avatar-bordered mt-4"
                size="72"
                :image="atividade.imagem"
              ></v-avatar>
            </v-col>
            <v-col cols="10" class="pl-6">
              <v-chip class="mt-3 mx-2" color="primary" text-color="white">{{ atividade.horario }}</v-chip>
              <v-card-title class="py-0 text-white" style="white-space: normal;">
                {{ atividade.titulo }}
              </v-card-title>
              <v-card-subtitle class="pt-0 text-white" style="white-space: normal;">
                {{ atividade.subtitulo }}
              </v-card-subtitle>
            </v-col>
          </v-row>
          <v-card-text class="text-white" style="font-size: 1.1em;">
            <strong>Convidado:</strong> {{ atividade.convidado }}<br>
            <strong>Minicurrículo:</strong> {{ atividade.minicurriculo }}<br><br>
            {{ atividade.descricao }}
          </v-card-text>
          <v-card-actions>
            <v-btn text color="primary" @click="atividade.expanded = !atividade.expanded">
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
      <v-col cols="12" md="6">
        <div class="pb-2">
          <span class="text-white text-h6">DOMINGO • 10.NOV</span>
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
            <v-col cols="2" class="pl-6">
              <v-avatar
                v-if="atividade.imagem"
                class="avatar-bordered mt-4"
                size="72"
                :image="atividade.imagem"
              ></v-avatar>
            </v-col>
            <v-col cols="10" class="pl-6">
              <v-chip class="mt-3 mx-2" color="primary" text-color="white">{{ atividade.horario }}</v-chip>
              <v-card-title class="py-0 text-white" style="white-space: normal;">
                {{ atividade.titulo }}
              </v-card-title>
              <v-card-subtitle class="pt-0 text-white" style="white-space: normal;">
                {{ atividade.subtitulo }}
              </v-card-subtitle>
            </v-col>
          </v-row>
          <v-card-text class="text-white" style="font-size: 1.1em;">
            <strong>Convidado:</strong> {{ atividade.convidado }}<br>
            <strong>Minicurrículo:</strong> {{ atividade.minicurriculo }}<br><br>
            {{ atividade.descricao }}
          </v-card-text>
          <v-card-actions>
            <v-btn text color="primary" @click="atividade.expanded = !atividade.expanded">
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
  </v-container>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const programacao = ref([]);

onMounted(async () => {
  try {
    const response = await fetch('./src/assets/programacao.json');
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
