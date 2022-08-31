<template>
  <v-btn
    @click="$vuetify.goTo('#home', { offset: 280 })"
    depressed
    icon
    fixed
    right
    bottom
    height="40px"
    width="40px"
    class="primary buttonUp"
  >
    <v-icon color="secondary" size="15">fa fa-arrow-up</v-icon>
  </v-btn>
</template>

<script>
export default {
  mounted() {
    document.addEventListener("scroll", this.onscroll);
  },
  methods: {
    onscroll() {
      const button = document.querySelector(".buttonUp");
      if (document.documentElement.scrollTop > 600) {
        button.style.pointerEvents = "all";
        button.style.opacity = "1";
      } else {
        button.style.pointerEvents = "none";
        button.style.opacity = "0";
      }
    },
  },
};
</script>

<style>
.buttonUp {
  opacity: 0;
  pointer-events: none;
  transition: all 0.45s;
  border-radius: 0 !important;
}
</style>
