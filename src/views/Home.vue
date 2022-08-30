<template>
  <v-sheet width="100%" height="300%" class="home secondary">
    <Hero />
    <Brands />
    <About />
    <Categories />
  </v-sheet>
</template>

<script>
import Hero from "./Hero.vue";
import Brands from "./Brands.vue";
import About from "./About.vue";
import Categories from "./Categories.vue";
export default {
  components: { Hero, Brands, About, Categories },
};
</script>
<style scoped>
.home {
  padding-top: 120px;
  height: 100%;
}
</style>
