<template>
  <div id="home" class="hero">
    <v-container>
      <v-row class="relative" align="center">
        <v-col class="d-flex flex-column white--text" lg="6" cols="12"
          ><div class="text-h2"><span class="outline-text">PEDALE</span></div>
          <div class="text-h1 mt-12">SUPER BIKES</div>
          <div class="text-body-1 w-60 mt-12">
            Pedalar nunca foi tão fácil e prazeroso. Transforme sua rotina
            pedalando diaramente.
          </div>
          <div>
            <v-btn
              href="#portfolio"
              height="58px"
              width="172px"
              class="secondary--text text-none text-body-2 font-weight-bold mt-12"
              color="primary"
              >Portfólio
              <v-icon size="15" class="ml-2">fa fa-arrow-right</v-icon></v-btn
            >
          </div></v-col
        >
        <v-col class="bg-hero-img" lg="6" cols="12">
          <img class="d-block hero-img" src="/img/bikes-top.png" alt="" />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {};
</script>

<style>
.relative {
  position: relative;
}
.bg-hero-img::after {
  z-index: 2;
  content: "";
  width: 612px;
  height: 780px;
  position: absolute;
  top: -220px;
  right: 0;
  background-image: url(/img/bg-hero.png);
}
.hero .v-btn {
  border-radius: 0 !important;
}
.w-60 {
  width: 60%;
}
.outline-text {
  color: transparent !important;
  font-weight: 900 !important;
  -webkit-text-stroke-width: 0.7px;
  -webkit-text-stroke-color: rgb(255, 255, 255);
}
.hero {
  margin-top: 100px;
}
.hero-img {
  z-index: 99;
  position: relative;
  margin-left: -70px !important;
  width: 125%;
  margin: auto;
  object-fit: contain;
  aspect-ratio: 711/542;
}
</style>
