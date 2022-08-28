<template>
  <div class="header">
    <Desktop v-if="!smAndDown" :menu="menu" />
    <Mobile v-if="smAndDown" :menu="menu" />
  </div>
</template>

<script>
import Desktop from "./Desktop.vue";
import Mobile from "./Mobile.vue";
export default {
  data: () => ({
    menu: [
      { name: "Home", link: "#home" },
      { name: "Sobre", link: "#about" },
      { name: "Categorias", link: "#categories" },
      { name: "Portfólio", link: "#portfolio" },
    ],
  }),
  components: { Desktop, Mobile },
  computed: {
    smAndDown() {
      return this.$vuetify.breakpoint.smAndDown;
    },
  },
};
</script>

<style>
.header {
  position: fixed !important;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 999;
}
</style>
