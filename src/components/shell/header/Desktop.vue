<template>
  <div>
    <v-sheet
      color="secondary"
      height="95px"
      class="d-flex align-center elevation-1 fixed"
    >
      <v-container class="py-0">
        <div class="d-flex justify-space-between align-center">
          <router-link to="#home">
            <img
              src="/img/bikeweb.svg"
              alt="Top Tintas"
              title="Top Tintas"
              class="d-block contain"
              height="45px"
            />
          </router-link>
          <div class="ml-auto">
            <div
              v-for="({ name, link }, key) in menu"
              :key="key"
              class="d-inline-flex"
            >
              <v-btn
                class="text-none px-2 px-lg-4 py-2 nav-link white--text text--darken-1"
                v-if="link"
                :to="link"
                tile
                depressed
                text
                active-class="secondary--text"
              >
                {{ name }}
              </v-btn>
            </div>
          </div>
        </div>
      </v-container>
    </v-sheet>
  </div>
</template>

<script>
export default {
  props: {},
  data: () => ({
    time: "",
    menu: [
      { name: "Home", link: "#home" },
      { name: "Sobre", link: "#about" },
      { name: "Categorias", link: "#categories" },
      { name: "Galeria", link: "#gallery" },
    ],
  }),
  computed: {},
};
</script>

<style>
.nav-link::before {
  opacity: 0 !important;
}

.v-btn--active .v-btn__content {
  color: #abdf3a !important;
}
/* .v-btn--active:after {
  content: "";
  display: block;
  width: 70%;
  height: 4px;
  background: #abdf3a;
  margin: 0 auto;
  margin-top: 150px;
  margin-bottom: 60px;
  position: absolute;
  border-radius: 2px;
  transition: all 0.5s linear !important;
} */
</style>
