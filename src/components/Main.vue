<template>
  <v-container class="fill-height">

    <v-row class="">
      <v-col md="5" cols="12">
        <v-img height="auto" src="@/assets/evento.jpeg" />
        <div class="pt-4">
          <!-- <v-btn
            color="yellow-darken-1"
            href="https://bit.ly/piumistico"
            size="x-large"
            target="_blank"
            variant="flat"
            class="mb-3"
            block
          > -->
          <v-btn
            color="yellow-darken-1"
            :to="linkProgramacao"
            size="x-large"
            target="_blank"
            variant="flat"
            class="mb-3"
            block
          >
            <v-icon
              icon="mdi-eye"
              size="large"
              start
            />
              Ver Programação
          </v-btn>
        </div>
        <v-container fluid class="px-0 ">
          <v-card class="px-0 mx-0" color="white">
            
            <!-- <v-card-title class="post-title">{{ postTitle }}</v-card-title> -->
            <v-responsive class="iframe-container">
              <!-- <img class="ratio" src="http://www.brightontheday.com/wp-content/uploads/2013/07/placeholder300.png" /> -->
              <iframe
                scrolling='no' 
                class=""
                :src="embedUrl"
                allow="autoplay; encrypted-media"
                allowfullscreen
              ></iframe>
            </v-responsive>
          </v-card>
        </v-container>
      </v-col>
      <v-col md="7" cols="12" class="text-white">
        <v-chip size="large" color="white" class="px-5 text-overline font-weight-bold">
          <v-icon class="pr-3">mdi-calendar</v-icon> 11, 12 e 13 de agosto
        </v-chip>
        <h1 class="pt-3 text-h1 text-yellow-darken-1">Pium Místico</h1>
        <h3 class="pt-3 text-h6 font-weight-regular">Prepare-se para três dias intensos de experiências enriquecedoras, conhecimentos ancestrais e práticas contemporâneas que irão expandir sua mente, corpo e espírito.</h3>
        <!-- <h3 class="pt-3 text-h6 font-weight-regular">O Pium Místico é um evento que transcende fronteiras, unindo saberes ancestrais e conhecimentos científicos atuais em uma experiência única.</h3> -->
        <h3 class="pt-3 text-h6 font-weight-regular">Nos dias 11, 12 e 13 de Agosto de 2023, no Espaço Mandalar, em Pium-RN, você terá a oportunidade de mergulhar em uma jornada profunda de conexão consigo mesmo(a) e com o planeta.</h3>
        <h3 class="pt-9 text-h4 font-weight-regular text-yellow-darken-1">Tema Central: A Integração do Ser e a Relação com o Planeta</h3>
        <h3 class="pt-3 text-h6 font-weight-regular">Explore a fascinante interligação entre o ser humano e o planeta em que vivemos. Nossos palestrantes, terapeutas e cientistas renomados irão conduzir discussões envolventes sobre como a harmonia entre nosso ser interior e a natureza ao nosso redor é fundamental para uma vida equilibrada e saudável.</h3>
        <h3 class="pt-9 text-h4 font-weight-regular text-yellow-darken-1">O Que Esperar</h3>
        <h3 class="pt-3 text-h6 font-weight-regular"><span class="text-yellow-darken-1">Palestras Inspiradoras:</span> Ouça vozes influentes do mundo holístico e científico compartilhando suas perspectivas sobre autoconhecimento, saúde integral e sustentabilidade.</h3>
        <h3 class="pt-3 text-h6 font-weight-regular"><span class="text-yellow-darken-1">Vivências Transformadoras:</span> Participe de práticas terapêuticas, meditações guiadas, danças sagradas e outras vivências que irão expandir sua consciência.</h3>
        <h3 class="pt-3 text-h6 font-weight-regular"><span class="text-yellow-darken-1">Feira de Gastronomia e Artesanato:</span> Delicie-se com opções saudáveis e saborosas enquanto explora criações artesanais inspiradoras.</h3>
        <h3 class="pt-3 text-h6 font-weight-regular"><span class="text-yellow-darken-1">Conexões Profundas:</span> Conheça pessoas afins e crie laços duradouros com uma comunidade unida pelo desejo de evolução e cura.</h3>
        <!-- <h3 class="pt-3 text-h6 font-weight-regular">Marcelo Kramer (@marcelokramerbr) - Explorador das conexões entre ciência, espiritualidade e tradições orientais. Instrutor de Yoga e Artes Marciais, pesquisador de Biologia Molecular nos EUA, também é praticante de tradições marciais japonesas e guerreiro místico, buscando otimizar a vida humana.</h3>
        <h3 class="pt-3 text-h6 font-weight-regular">Dra. Kássia Galvão - Médica formada pela UFAC, especializada em Medicina Funcional e Integrativa. Com vasta experiência em saúde e autoconhecimento, possui pós-graduações em Nutrologia, Medicina da Família e Comunidade, Neurociências e Práticas Meditativas, e Adequação Nutricional.</h3>
        <h3 class="pt-3 text-h6 font-weight-regular">André Ortega (@andreortega.oficial) - Estudioso vegano apaixonado por tecnologia e tradições antigas. Bacharel em Sistemas de Informação, é especialista em Dashboard Data Marketing Analytics e Customer Experience Automation. Seu foco de estudo inclui chakras, mantras, cosmologia e a comunidade Essênia.</h3>
        <h3 class="pt-3 text-h6 font-weight-regular">Carlos Magno - Doutor em Ciências Climáticas, Mestre e graduado em Física. Professor de física, educação e meio ambiente no Instituto Federal do RN. Há anos estuda o comportamento da sociedade em relação ao ambiente, e é autor de livros sobre conscientização ambiental e mudanças climáticas.</h3>
        <h3 class="pt-3 text-h6 font-weight-regular">Samelly Xavier - Escritora, astróloga e oraculista. Conduzirá um minicurso sobre inteligência existencial, explorando temas como inteligências múltiplas, chakraterapia e relacionamentos, visando aprofundar a conexão com corpo, alma e coração.</h3>
        <h3 class="pt-3 text-h6 font-weight-regular">Marcos Cabral (@marcoscabral.sistemico) - Especialista em Constelação Sistêmica, Marcos explorará a relação entre dores físicas e emocionais, conduzindo uma jornada de compreensão e cura através dessa abordagem.</h3>
        <h3 class="pt-3 text-h6 font-weight-regular">Letícia Souto (@luarbelezaholistica) - Terapeuta holística, instrutora de yoga, guardiã do projeto Roda das Sábias e idealizadora da Luar Beleza Holística. Letícia é uma sacerdotisa dedicada a auxiliar mulheres em sua jornada de autodescoberta e despertar.</h3>
        <h3 class="pt-3 text-h6 font-weight-regular">Talita Costa (@talitacostaterapeuta) - Conhecida como Bruxa Ãnanda multidimensional, Talita é mestra em Reiki, guardiã de massagem energética vibracional e co-criadora do TantraSER. Sua jornada terapêutica se estende por 18 anos, auxiliando no despertar da consciência e cura da alma.</h3>
        <h3 class="pt-3 text-h6 font-weight-regular">Tatiana Gaeta (@nutritatianagaeta) - Nutricionista clínica especializada em nutrição integrativa vegana. Mestre em Usui Reiki Ryoho e membro da ABRATH, Tatiana atua na Casa Mandala Espaço Holístico, onde oferece terapias energéticas e ministra cursos.</h3>
        <h3 class="pt-3 text-h6 font-weight-regular">Juliana Iyafemi (@ventosdecura_) - Aromaterapeuta, doula, parteira aprendiz e instrutora de ThetaHealing®, Juliana é uma praticante dedicada de diversas terapias, incluindo dança, yoga, reiki e capoeira angola. Sua busca pelo autoconhecimento a levou a explorar diferentes abordagens de cura.</h3>
        <h3 class="pt-3 text-h6 font-weight-regular">Deva Arya - Terapeuta cósmica e guardiã da Casa Casulo, Deva Arya canaliza o método TantraSer, unindo ferramentas do tantra ancestral e xamânico para despertar a energia vital e desenvolver o ser em toda a sua potência.</h3> -->
        <h3 class="pt-9 text-h4 font-weight-regular text-yellow-darken-1">Aproveite a Oportunidade de Transformação!</h3>
        <!-- <h3 class="pt-3 text-h6 font-weight-regular">Garanta seu passaporte único para os 3 dias de imersão no Pium Místico. Aproveite o valor promocional e faça parte deste evento que irá expandir sua consciência, trazer clareza e inspiração para sua jornada de vida. Junte-se a nós nessa busca pela cura integral do ser e pela harmonia com o planeta. Sua transformação começa aqui!</h3> -->
        <!-- <h3 class="pt-9 text-h4 font-weight-regular text-yellow-darken-1">Reserve Agora!</h3> -->
        <div class="pt-4 pb-16">
          <v-btn
            block
            color="yellow-darken-1"
            :href="linkProgramacao"
            target="_blank"
            min-width="228"
            size="x-large"
            variant="outlined"
            class="mb-3"
          >
            <v-icon
              icon="mdi-eye"
              size="large"
              start
            />
              Ver Programação Completa
          </v-btn>
          <v-btn
            block
            color="yellow-darken-1"
            href="https://wa.me/+5584986009104?text=Ol%C3%A1,%20Hannah,%20estou%20vindo%20do%20site%20e%20gostaria%20de%20reservar%20meu%20ingresso"
            min-width="228"
            size="x-large"
            target="_blank"
            variant="flat"
            class="mb-3"
          >
              Reservar
          </v-btn>
        </div>
      </v-col>
    </v-row>
    
  </v-container>
</template>

<style>
/* .iframe-container {
  position: relative;
  width: 100%;
  padding-top: 56.25%; /* Proporção 16:9 (dividir a altura pelo width e multiplicar por 100) 
} */

/* .responsive-iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
} */

/* .iframe-container {
	position: relative;
	padding-bottom: 56.25%;
	padding-top: 25px;
	height: 0;
} /* 16:9 */
/* .responsive-iframe iframe {
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
} */

.iframe-container {
  overflow: hidden;
  /* padding-top: 56.25%; 16:9 */
  padding-top: 190%; /* 9:16 */
  position: relative;
} 

.iframe-container iframe {
  position: absolute;
  top: 0;
  left: 0;
  border: 0;
  width: 100%;
  height: 100%;
}
</style>

<script setup>
import { computed } from 'vue';

const postTitle = "Hannah explica o evento Pium Místico na Rádio Mar e Campo"; // Substitua pelo título real do post do Instagram
//const linkProgramacao = "https://bit.ly/piumistico";
const linkProgramacao = "/programacao-pium-mistico";

const embedUrl = computed(() => {
  // Substitua "VIDEO_ID" pelo ID do vídeo do Instagram que você deseja incorporar
  const videoId = "CvkFoqbO1lg";
  return `https://www.instagram.com/p/${videoId}/embed/`;
})
</script>
