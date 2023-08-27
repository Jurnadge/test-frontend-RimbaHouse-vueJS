<script>
import Card from "./Card.vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import { tvShowData } from "../assets/fakeData";
import "swiper/css";
import "swiper/css/pagination";
import { Pagination } from "swiper/modules";

export default {
  name: "MovieList",
  components: { Card, Swiper, SwiperSlide, Pagination },
  data() {
    return {
      tvShow: tvShowData,
    };
  },
  setup() {
    return {
      modules: [Pagination],
    };
  },
};
</script>

<template>
  <div class="text-white mx-8 h-screen mt-4 lg:mt-10">
    <div>
      <h1>TV Series</h1>
      <swiper
        :slidesPerView="1"
        :spaceBetween="10"
        :pagination="{
          clickable: true,
        }"
        :breakpoints="{
          '@0.00': {
            slidesPerView: 3,
            spaceBetween: 10,
          },
          '@0.75': {
            slidesPerView: 4,
            spaceBetween: 20,
          },
          '@1.00': {
            slidesPerView: 4,
            spaceBetween: 40,
          },
          '@1.50': {
            slidesPerView: 5,
            spaceBetween: 50,
          },
        }"
        :modules="modules"
        class="mySwiper"
      >
        <swiper-slide v-for="(show, index) in tvShow" :key="index"
          ><Card :img="show.img" :title="show.movieTitle" :year="show.year"
        /></swiper-slide>
      </swiper>
    </div>

    <div>
      <h1>TV Series</h1>
      <swiper
        :slidesPerView="1"
        :spaceBetween="10"
        :pagination="{
          clickable: true,
        }"
        :breakpoints="{
          '@0.00': {
            slidesPerView: 3,
            spaceBetween: 10,
          },
          '@0.75': {
            slidesPerView: 4,
            spaceBetween: 20,
          },
          '@1.00': {
            slidesPerView: 4,
            spaceBetween: 40,
          },
          '@1.50': {
            slidesPerView: 5,
            spaceBetween: 50,
          },
        }"
        :modules="modules"
        class="mySwiper"
      >
        <swiper-slide v-for="(show, index) in tvShow" :key="index"
          ><Card :img="show.img" :title="show.movieTitle" :year="show.year"
        /></swiper-slide>
      </swiper>
    </div>
  </div>
</template>
