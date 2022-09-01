<template>
  <v-container
    class="px-lg-0 px-md-0 mt-lg-16 mt-md-16 mt-5 pt-lg-16 pt-md-16 pt-6"
  >
    <div
      id="portfolio"
      class="d-flex justify-center flex-column align-center mt-5"
    >
      <SubTitle>Portfólio</SubTitle>
      <div class="text-h4 white--text mt-5 text-center mb-lg-16 mb-md-16 mb-5">
        <span class="outline-text">VIVA</span> NOSSAS HISTÓRIAS
      </div>
    </div>
    <div class="portfolio mt-9">
      <div class="item" v-for="(item, key) in thumbs" :key="key">
        <a
          class="text-decoration-none"
          href="javascript:void(0);"
          @click="
            images = images;
            index = key;
          "
        >
          <img width="100%" :src="item.url" v-if="item.url" class="d-block" />
        </a>
      </div>
      <LightGallery
        interfaceColor="#ABDF3A"
        :images="images"
        :index="index"
        :disable-scroll="true"
        @close="index = null"
      />
    </div>
  </v-container>
</template>

<script>
import { LightGallery } from "vue-light-gallery";
import SubTitle from "../../components/SubTitle.vue";

export default {
  components: {
    SubTitle,
    LightGallery,
  },
  data() {
    return {
      thumbs: [
        { title: "Praia", url: "/img/portfolio/bike-beach.jpg" },
        { title: "Estrada", url: "/img/portfolio/bike-road.jpg" },
        { title: "corrida", url: "/img/portfolio/bike-roadway.jpg" },
      ],
      images: [
        { title: "Praia", url: "/img/portfolio/bike-beach.jpg" },
        { title: "Estrada", url: "/img/portfolio/bike-road.jpg" },
        { title: "corrida", url: "/img/portfolio/bike-roadway.jpg" },
        { title: "Capacete", url: "/img/portfolio/bike-helmet.jpg" },
        { title: "Catraca", url: "/img/portfolio/bike-wheel.jpg" },
        { title: "Trilha", url: "/img/portfolio/bike-downhill.png" },
      ],
      index: null,
    };
  },
};
</script>

<style>
.portfolio {
  display: flex;
  gap: 30px;
}
.portfolio .item {
width:100%;
}
.portfolio .item:nth-child(1) {
width:50%;
}
.item {
  height: 330px;
  flex: 1 1 500px;
}
.item img {
  height: 100%;
  object-fit: cover;
  object-position: center;
}
.light-gallery__close,
.light-gallery__next,
.light-gallery__prev {
  opacity: 0.8;
  background-color: #abdf3a !important;
  color: #121717 !important;
}
.light-gallery__close g,
.light-gallery__next polyline,
.light-gallery__prev polyline {
  stroke: #121717 !important;
}
</style>
