<script setup>
import { Slide } from "../data.js";
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/navigation";
import "swiper/css/pagination";

// import required modules
import { Navigation, Pagination, Mousewheel, Keyboard } from "swiper/modules";
const modules = [Navigation, Pagination, Mousewheel, Keyboard];
</script>
<template>
  <section class=" flex place-content-around">
    <div class="flex flex-col items-center place-content-around mb-28 w-[80%]">
      <div class=" font-medium text-3xl" data-aos="fade-down">Experience</div>
      <swiper
        :cssMode="true"
        :navigation="true"
        :pagination="{
          clickable: true,
        }"
        :mousewheel="true"
        :keyboard="{
          enabled: true,
        }"
        :modules="modules"
        class="mySwiper"
        data-aos="fade-down"
      >
        <swiper-slide v-for="(slide, index) in Slide" :key="index" >
          <div class="mt-10">
            <div class="flex place-content-around">
              <img
                class=" object-fill bg-cover hover:object-scale-down h-full max-h-96 max-w-[30%] pb-5"
                :src="slide.img"
                alt="{{ slide.name }}"
              />
            </div>
            <h2 class="flex place-content-around text-2xl font-semibold">
              {{ slide.name }}
            </h2>
            <p class="mt-2 text-xs">{{ slide.description }}</p>
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </section>
</template>
