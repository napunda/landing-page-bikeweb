<template>
  <div class="mt-16 pt-6 d-flex justify-center">
    <v-container class="pa-0 ma-0">
      <div
        id="categories"
        class="d-flex justify-center flex-column align-center"
      >
        <SubTitle>Categorias</SubTitle>
        <div class="text-h4 white--text mt-5 text-center mb-16">
          <span class="outline-text">CONHEÇA</span> NOSSA LINHA
        </div>
      </div>
      <div class="category-container justify-lg-space-between justify-center">
        <div
          class="content d-flex white--text"
          v-for="({ icon, title, text }, key) in categories"
          :key="key"
        >
          <div class="content-img">
            <img :src="icon" :alt="title" />
          </div>
          <div class="text-lg-h5 text-body-2 mt-5 mb-5 font-weight-bold">
            {{ title }}
          </div>
          <div class="text-body-1 caption-categories">{{ text }}</div>
          <v-btn color="white" v-ripple="false" class="arrow-icon" text icon>
            <v-icon size="15px" color="#1B201C">fa fa-arrow-right</v-icon>
          </v-btn>
        </div>
      </div>
    </v-container>
  </div>
</template>

<script>
import SubTitle from "../components/SubTitle.vue";
export default {
  data: () => ({
    categories: [
      {
        icon: "/img/icons/passeio.svg",
        title: "Passeio",
        text: "O cuidado em identificar pontos críticos na contínua expansão de nossa atividade faz parte de um processo de gerenciamento de alternativas às soluções ortodoxas.",
      },
      {
        icon: "/img/icons/esporte.svg",
        title: "Esporte",
        text: "Pensando mais a longo prazo, a percepção das dificuldades faz parte de um processo de gerenciamento das diretrizes de desenvolvimento para o futuro.",
      },
      {
        icon: "/img/icons/lazer.svg",
        title: "Lazer",
        text: "As bicicletas para conforto e lazer  são fabricadas para aquilo que o ciclismo realmente deve ser: ​​a alegria de subir na sua bike e ir embora, só pela diversão.",
      },
      {
        icon: "/img/icons/trabalho.svg",
        title: "Trabalho",
        text: "A alta praticidade e funcionalidade das bikes têm feito delas um grande investimento de meio de locomoção para o trabalho.",
      },
    ],
  }),
  components: { SubTitle },
};
</script>

<style>
.caption-categories {
  color: rgba(255, 255, 255, 0.7);
  transition: all ease-in-out 0.5s;
}
.arrow-icon {
  position: absolute;
  bottom: 20px;
  right: 20px;
  border-radius: 0 !important;
  opacity: 0;
  transition: all ease-in-out 0.5s;
}
.category-container {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}
.content {
  position: relative;
  max-height: 330px;
  aspect-ratio: 276/330;
  background-color: #1b201c;
  padding: 20px;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  transition: all ease-in-out 0.5s;
}
.content:hover {
  background-color: #799e29;
  color: #1b201c !important;
  outline: 0.5px solid rgba(255, 255, 255, 0.548);
}
.content:hover .arrow-icon {
  opacity: 1;
}
.content:hover .caption-categories {
  color: #1b201c;
}
.content-img {
  height: 60px;
  display: flex;
  align-items: center;
  justify-content: center;
  aspect-ratio: 60/60;
  background-color: #fff;
  border-radius: 50%;
  opacity: 0.7;
  padding: 10px;
}
.content-img img {
  object-fit: contain;
  width: 100%;
  transition: all ease-in-out 0.5s;
}
</style>
