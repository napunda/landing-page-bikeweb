<template>
  <v-container class="mt-lg-16 mt-md-16 mt-5 pb-lg-16 pb-md-16 pb-5">
    <div id="about" class="d-flex justify-center flex-column align-center">
      <SubTitle>Sobre nós</SubTitle>
      <div class="text-h4 white--text mt-5 text-center mb-lg-16 mb-md-16 mb-5">
        <span class="outline-text">QUEM SOMOS</span> E CONSTRUIMOS
      </div>
    </div>
    <div class="d-flex justify-center mt-9">
      <img class="d-block" width="70%" src="/img/logo-about.svg" alt="Logo" />
    </div>
    <v-row>
      <v-col
        class="white--text d-flex flex-column align-center text-center"
        cols="4"
      >
        <div id="technology" class="text-lg-h6 mt-5 mb-2 font-weight-bold">
          TECNOLOGIA
        </div>
        <div class="text-lg-body-1 text-md-body-1 text-caption">
          A inovação que traz confiava e conforto também preza pelos comodidade
          na hora de comprar.
        </div>
      </v-col>
      <v-col
        class="white--text d-flex flex-column align-center text-center"
        cols="4"
      >
        <div id="innovation" class="text-lg-h6 mt-5 mb-2 font-weight-bold">
          INOVAÇÃO
        </div>
        <div class="text-lg-body-1 text-md-body-1 text-caption">
          Amostra de produtos ainda poucos conhecidos no mercado, porém com alta
          confibilidade.
        </div>
      </v-col>
      <v-col
        class="white--text d-flex flex-column align-center text-center"
        cols="4"
      >
        <div id="convenience" class="text-lg-h6 mt-5 mb-2 font-weight-bold">
          COMODIDADE
        </div>
        <div class="text-lg-body-1 text-md-body-1 text-caption">
          A inovação que traz confiava e conforto também preza pelos comodidade
          na hora de comprar.
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import SubTitle from "../../components/SubTitle.vue";
export default { components: { SubTitle } };
</script>

<style></style>
