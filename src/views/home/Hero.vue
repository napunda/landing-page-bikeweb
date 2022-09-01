<template>
  <div id="home" class="hero">
    <v-container v-if="!smAndDown">
      <v-row class="relative" align="center">
        <v-col class="d-flex flex-column white--text" lg="6" cols="12">
          <div class="text-h2">
            <span class="outline-text">PEDALE</span>
          </div>
          <div class="text-h1 mt-12">SUPER BIKES</div>
          <div class="text-body-1 w-60 mt-12">
            Pedalar nunca foi tão fácil e prazeroso. Transforme sua rotina
            pedalando diaramente.
          </div>
          <div>
            <v-btn
              @click="$vuetify.goTo('#portfolio', { offset: 300 })"
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
    <v-container v-else>
      <v-row class="relative hero-img-mobile" align="center">
        <v-col class="d-flex flex-column white--text" cols="12">
          <div class="text-h4 text-md-h3">
            <span class="outline-text">PEDALE</span>
          </div>
          <div class="mt-5 mt-md-10 text-h3 text-md-h2 font-weight-bold">
            SUPER BIKES
          </div>
          <div class="text-body-1 w-60 mt-5 mt-md-10">
            Pedalar nunca foi tão fácil e prazeroso. Transforme sua rotina
            pedalando diaramente.
          </div>
          <div>
            <v-btn
              @click="$vuetify.goTo('#portfolio', { offset: 300 })"
              :height="!xs ? `58px` : `40px`"
              :width="!xs ? `172px` : `100px`"
              class="secondary--text text-none text-md-body-2 text-sm-body-2 text-caption font-weight-bold mt-5 mt-md-10"
              color="primary"
              >Portfólio
              <v-icon :size="!xs ? `15` : `10`" class="ml-2"
                >fa fa-arrow-right</v-icon
              ></v-btn
            >
          </div></v-col
        >
        <v-col cols="12">
          <img width="100%" class="d-block" src="/img/bikes-top.png" alt="" />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  computed: {
    smAndDown() {
      return this.$vuetify.breakpoint.mdAndDown;
    },
    xs() {
      return this.$vuetify.breakpoint.xsOnly;
    },
  },
};
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
@media (max-width: 1000px) {
  .hero {
    margin-top: 0px !important;
  }
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
.hero-img-mobile {
  position: relative;
}
.hero-img-mobile {
  background-position: right;
  background-image: url(/img/bg-hero-mobile.svg);
  background-size: contain;
}
</style>
