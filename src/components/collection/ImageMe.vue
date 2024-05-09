<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";
import "swiper/css/effect-coverflow";
import "swiper/css/pagination";
import "swiper/css/navigation";
import { imageOfMe } from "./imageMe";
import Footer from "../Footer.vue";

// import required modules
import {
  Autoplay,
  Pagination,
  Navigation,
  EffectCoverflow,
} from "swiper/modules";
import Navbar from "../Navbar.vue";

const modules = [Navigation, Pagination, Autoplay, EffectCoverflow];
</script>
<template>
  <section class=" ">
    <div class="flex place-content-around text-2xl font-semibold m-3">
      <h1>My photo collection</h1>
    </div>
    <div class="flex place-content-around">
      <div class="w-[80%]">
        <swiper
          :spaceBetween="30"
          :centeredSlides="true"
          :autoplay="{
            delay: 2500,
            disableOnInteraction: false,
          }"
          :pagination="{
            clickable: true,
          }"
          :navigation="true"
          :modules="modules"
          @autoplayTimeLeft="onAutoplayTimeLeft"
          class="mySwiper"
        >
          <swiper-slide class="mt-1 mb-10">
            <h1>Title</h1>
            <div>
              <p>this is home</p>
            </div>
            <div>find the new procees</div>
          </swiper-slide>
          <swiper-slide>Slide 2</swiper-slide>
        </swiper>
      </div>
    </div>
    <div class="flex place-content-around">
      <div class="sm:w-3/5 md:w-2/5 xl:w-1/5">
        <swiper
          :effect="'coverflow'"
          :grabCursor="true"
          :centeredSlides="true"
          :slidesPerView="'auto'"
          :coverflowEffect="{
            rotate: 50,
            stretch: 0,
            depth: 100,
            modifier: 1,
            slideShadows: true,
          }"
          :pagination="true"
          :modules="modules"
          class="mySwiper"
        >
          <swiper-slide
            v-for="(item, index) in imageOfMe"
            :key="index"
            class=""
          >
            <img :src="item.img" class=" " />
          </swiper-slide>
        </swiper>
      </div>
    </div>
  </section>
  <div class="z-10 mt-4 sticky">
    <Navbar />
  </div>
  <div class="z-0 mt-2">
    <Footer class="z-50" />
  </div>
</template>
