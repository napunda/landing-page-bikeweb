<template>
  <v-sheet color="transparent" class="mt-150 pb-6 footer">
    <v-container class="pa-lg-0">
      <footer>
        <v-row>
          <v-col cols="12" lg="0" md="6">
            <img height="50px" class="d-block" src="/img/logo.svg" alt="" />
            <div class="white--text text-body-1 mt-5 mb-5 caption-news-letter">
              Mantenha-se informado sobre lançamentos.
            </div>
            <div class="d-flex news-letter my-6">
              <v-text-field
                light
                hide-details
                class="white--text"
                color="primary"
                outlined
                dense
                height="50px"
                label="Seu e-mail"
                single-line
              ></v-text-field>
              <v-btn
                height="50px"
                class="secondary--text ml-4 text-none px-11 text-body-2"
                color="primary"
                >Inscrever</v-btn
              >
            </div>
          </v-col>
          <v-col cols="12" lg="0" md="6">
            <v-row>
              <v-col
                v-for="({ title, menus }, key) in menuFooter"
                :key="key"
                cols="4"
              >
                <div class="text-lg-h6 white--text mb-8 font-weight-bold">
                  {{ title }}
                </div>
                <div
                  class="d-flex flex-column justify-start align-start links-footer"
                >
                  <v-btn
                    class="white--text text-none text-body-1 text-opacity-60"
                    v-for="({ title, link }, key) in menus"
                    :key="key"
                    text
                    @click="$vuetify.goTo(link, { offset: 120 })"
                  >
                    {{ title }}
                  </v-btn>
                </div>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
        <div class="copy white--text mt-lg-16 mt-md-16 mt-5 pt-9">
          <div class="text-body-1 text-center text-opacity-60">
            BikeWeb 2022 - Todos os direitos reservados.
          </div>
          <div class="d-flex justify-center">
            <v-btn
              target="_blank"
              href="https://facebook.com"
              class="ml-5"
              fab
              dark
              small
              color="primary"
            >
              <v-icon color="secondary" size="18">fa fa-facebook</v-icon>
            </v-btn>
            <v-btn
              target="_blank"
              href="https://twitter.com"
              class="ml-5"
              fab
              dark
              small
              color="primary"
            >
              <v-icon color="secondary" size="18">fa fa-twitter</v-icon>
            </v-btn>
            <v-btn
              target="_blank"
              href="https://instagram.com"
              class="ml-5"
              fab
              dark
              small
              color="primary"
            >
              <v-icon color="secondary" size="18">fa fa-instagram</v-icon>
            </v-btn>
          </div>
        </div>
      </footer>
    </v-container>
  </v-sheet>
</template>

<script>
export default {
  data: () => ({
    menuFooter: [
      {
        title: "SOBRE",
        menus: [
          { title: "Tecnologia", link: "#about" },
          { title: "Inovação", link: "#about" },
          { title: "Comodidade", link: "#about" },
        ],
      },
      {
        title: "CATEGORIAS",
        menus: [
          { title: "Passeio", link: "#categories" },
          { title: "Esporte", link: "#categories" },
          { title: "Lazer", link: "#categories" },
          { title: "Trabalho", link: "#categories" },
        ],
      },
      {
        title: "MENU",
        menus: [
          { title: "Topo", link: "#top" },
          { title: "Marcas", link: "#brands" },
          { title: "Galeria", link: "#portfolio" },
        ],
      },
    ],
  }),
};
</script>

<style>
.mt-150 {
  margin-top: 150px;
}
@media (max-width: 960px) {
  .mt-150 {
    margin-top: 36px;
  }
}
.text-opacity-60 {
  opacity: 0.6 !important;
}
.links-footer .v-btn {
  border-radius: 0px;
  padding: 0 !important;
  min-width: 100% !important;
  justify-content: flex-start;
}
.news-letter .v-text-field,
.news-letter .v-btn {
  border-radius: 0 !important ;
}
.theme--light.v-text-field--outlined:not(.v-input--is-focused):not(.v-input--has-state)
  > .v-input__control
  > .v-input__slot
  fieldset {
  border-radius: 0 !important;
  color: #abdf3a !important;
}
.theme--light.v-input input,
.theme--light.v-input textarea,
.v-label {
  color: #fff !important;
}
.v-label {
  opacity: 0.6;
  position: inherit !important;
  width: 100% !important;
  top: 0 !important;
}
.news-letter {
  width: 71%;
}
@media (max-width: 960px) {
  .news-letter,
  .caption-news-letter {
    width: 100% !important;
  }
}
.caption-news-letter {
  width: 35%;
}
.copy {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap-reverse;
  gap: 20px;
}
@media (max-width: 600px) {
  .copy {
    width: 100% !important;
    justify-content: center;
  }
}
</style>
