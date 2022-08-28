<template>
  <div>
    <v-sheet
      color="secondary"
      height="120px"
      class="d-flex align-center elevation-1 fixed"
    >
      <v-container class="pa-lg-0">
        <div class="d-flex justify-space-between align-center">
          <router-link to="#home">
            <img
              src="/img/logo.svg"
              alt="Top Tintas"
              title="Top Tintas"
              class="d-block contain"
              height="50.25px"
            />
          </router-link>
          <div class="ml-auto">
            <div
              v-for="({ name, link }, key) in menu"
              :key="key"
              class="d-inline-flex nav"
            >
              <v-btn
                class="text-none mx-lg-8 mx-3 py-2 nav-link white--text text--darken-1 text-lg-h5 text-body-2"
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
  props: {
    menu: {
      type: Array,
      default: () => [],
    },
  },
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
.nav:nth-child(4) a {
  color: #121717 !important;
  font-weight: 700;
  width: 172px !important;
  height: 58px !important;
  margin-left: 52px;
  margin-right: 0 !important;
  background-color: #ffffff;
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
