<template>
  <v-sheet width="100%" height="300%" class="home secondary">
    <Hero />
    <Brands />
    <About />
  </v-sheet>
</template>

<script>
import Hero from "./Hero.vue";
import Brands from "./Brands.vue";
import About from "./About.vue";
export default {
  components: { Hero, Brands, About },
};
</script>
<style scoped>
.home {
  padding-top: 120px;
  height: 100%;
}
</style>
