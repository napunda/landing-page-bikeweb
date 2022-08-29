<template>
  <v-app>
    <Header />
    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
import Header from "./components/shell/header/Index.vue";
export default {
  data: () => ({
    //
  }),
  components: { Header },
};
</script>
<style>
.Kaushan-Script {
  font-family: "Kaushan Script", cursive;
}

@media screen and (min-width: 1200px) {
  .container {
    max-width: 1194px !important;
  }
}
</style>
