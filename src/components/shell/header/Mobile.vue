<template>
  <div>
    <v-app-bar class="secondary main-header-mobile elevation-4" app>
      <div class="py-2 d-flex align-end">
        <router-link class="d-flex" to="/">
          <img src="/img/logo.svg" alt="Logo" class="navbar-brand" />
        </router-link>
      </div>

      <v-spacer />

      <v-app-bar-nav-icon
        color="white"
        @click="drawer = !drawer"
      ></v-app-bar-nav-icon>
    </v-app-bar>

    <v-navigation-drawer class="blur" v-model="drawer" fixed temporary>
      <div class="px-8 py-6 d-flex flex-column">
        <router-link to="/" class="d-flex">
          <img
            width="100%"
            src="/img/logo.svg"
            alt="Logo"
            class="mx-auto fill-invert"
          />
        </router-link>
      </div>

      <v-list-item-group v-model="current">
        <v-list>
          <div v-for="({ name, link }, i) in menu" :key="i">
            <v-list-item
              @click="$vuetify.goTo(link, { offset: 200 })"
              v-if="link"
              :to="link"
              link
            >
              <v-list-item-content>
                <v-list-item-title
                  class="white--text text-body-2 font-weight-medium nav-link"
                >
                  {{ name }}
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </div>
        </v-list>
      </v-list-item-group>
    </v-navigation-drawer>
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
  data() {
    return {
      current: this.$route.path,
      drawer: false,
    };
  },
};
</script>

<style scoped>
.nav-link .icon {
  vertical-align: baseline;
}
</style>

<style>
.fill-invert {
  filter: brightness(0) invert(1);
}
.main-header-mobile {
  z-index: 610 !important;
}

.main-header-mobile .navbar-brand {
  height: 30px;
}

.v-navigation-drawer__content .navbar-brand {
  height: 100px;
}

.v-navigation-drawer {
  z-index: 620 !important;
}

.v-list-item__icon .v-icon {
  color: #ffffff !important;
  font-size: 14px !important;
}
.blur {
  background-color: #121717e7 !important;
}
</style>
