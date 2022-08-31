<template>
  <v-sheet width="100%" class="home secondary">
    <Hero />
    <Brands />
    <About />
    <Categories />
    <Portfolio />
    <Footer />
    <ButtonScrollUp />
  </v-sheet>
</template>

<script>
import Hero from "./Hero.vue";
import Brands from "./Brands.vue";
import About from "./About.vue";
import Categories from "./Categories.vue";
import ButtonScrollUp from "../../components/ButtonScrollUp.vue";
import Portfolio from "./Portfolio.vue";
import Footer from "../../components/shell/footer/Footer.vue";
export default {
  components: {
    Hero,
    Brands,
    About,
    Categories,
    ButtonScrollUp,
    Portfolio,
    Footer,
  },
};
</script>
<style scoped>
.home {
  padding-top: 120px;
  height: 100%;
}
</style>
