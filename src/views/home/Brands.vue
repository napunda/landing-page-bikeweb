<template>
  <v-sheet id="brands" color="transparent" class="brands mt-6">
    <v-container>
      <hooper ref="customersCarousel" :settings="hooperSettings">
        <slide v-for="({ src, name }, key) in brands" :key="key">
          <div class="brands-items">
            <img width="100%" :src="src" :alt="name" />
          </div>
        </slide>
      </hooper>
    </v-container>
  </v-sheet>
</template>

<script>
import { Hooper, Slide } from "hooper";
import "hooper/dist/hooper.css";
export default {
  data: () => ({
    hooperSettings: {
      infiniteScroll: true,
      wheelControl: false,
      autoPlay: false,
      itemsToSlide: 1,
      breakpoints: {
        0: {
          itemsToShow: 2,
        },
        600: {
          itemsToShow: 2,
        },
        800: {
          itemsToShow: 3,
        },
        1000: {
          itemsToShow: 4,
        },
      },
    },
    brands: [
      { src: "/img/caloi.png", name: "Caloi" },
      { src: "/img/colli.png", name: "Colli" },
      { src: "/img/ksw.png", name: "Ksw" },
      { src: "/img/rino.png", name: "Rino" },
    ],
  }),
  components: {
    Hooper,
    Slide,
  },
};
</script>

<style>
.hooper-list:focus-visible {
  outline: none !important;
}
.hooper {
  height: 100%;
}
.brands-items {
  height: 62px;
  width: 170px;
}
.brands img,
.brands a img {
  width: 100%;
  height: 100%;
  object-fit: contain !important;
  filter: brightness(0) invert(1);
  opacity: 0.25;
  transition: all 0.55s;
}
.brands img:hover {
  filter: none;
  opacity: 1;
}
</style>
