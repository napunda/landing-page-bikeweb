<template>
  <v-container class="mt-lg-16 mt-md-16 mt-5 pb-lg-16 pb-md-16 pb-5">
    <div id="about" class="d-flex justify-center flex-column align-center">
      <SubTitle>Sobre nós</SubTitle>
      <div class="text-h4 white--text mt-5 text-center mb-lg-16 mb-md-16 mb-5">
        <span class="outline-text">QUEM SOMOS</span> E CONSTRUIMOS
      </div>
    </div>
    <div class="row-about mt-lg-16 mt-6">
      <div
        class="white--text d-flex flex-column align-center text-center item-about"
      >
        <img class="d-block" width="100%" src="/img/icons/tec.svg" alt="" />
        <div class="negative-margin">
          <div id="technology" class="text-lg-h6 mt-5 mb-2 font-weight-bold">
            TECNOLOGIA
          </div>
          <div class="text-lg-body-1 text-md-body-1 text-caption px-5">
            Bicicletas desenvolvidas com alta tecnologia para o melhor
            desempenho em cada finalidade.
          </div>
        </div>
      </div>
      <div
        class="white--text d-flex flex-column align-center text-center item-about"
      >
        <img class="d-block" width="100%" src="/img/icons/inov.svg" alt="" />
        <div class="negative-margin">
          <div id="innovation" class="text-lg-h6 mt-5 mb-2 font-weight-bold">
            INOVAÇÃO
          </div>
          <div class="text-lg-body-1 text-md-body-1 text-caption px-5">
            Amostra de produtos ainda poucos conhecidos no mercado, porém com
            alta confibilidade.
          </div>
        </div>
      </div>
      <div
        class="white--text d-flex flex-column align-center text-center item-about"
      >
        <img class="d-block" width="100%" src="/img/icons/como.svg" alt="" />
        <div class="negative-margin">
          <div id="convenience" class="text-lg-h6 mt-5 mb-2 font-weight-bold">
            COMODIDADE
          </div>
          <div class="text-lg-body-1 text-md-body-1 text-caption px-5">
            A inovação que traz confiava e conforto também preza pelos
            comodidade na hora de comprar.
          </div>
        </div>
      </div>
    </div>
  </v-container>
</template>

<script>
import SubTitle from "../../components/SubTitle.vue";
export default { components: { SubTitle } };
</script>

<style>
.row-about {
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
  justify-content: space-around;
}
.item-about {
  max-width: 350px;
}
.negative-margin {
  margin-top: -225px;
  margin-bottom: 200px;
}
</style>
