<script setup>
import { Slide } from "../data.js";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import { Navigation, Pagination, Mousewheel, Keyboard } from "swiper/modules";
import { ref } from "vue";

const modules = [Navigation, Pagination, Mousewheel, Keyboard];
const dialogOpen = ref(false);
const selectedSlide = ref(null);

function openDialog(slide) {
  selectedSlide.value = slide;
  dialogOpen.value = true;
}

function closeDialog() {
  dialogOpen.value = false;
}
</script>

<template>
  <section id="experience" class="flex place-content-around z-10">
    <div class="flex flex-col items-center place-content-around mb-28 w-[80%]">
      <div class="font-medium text-3xl" data-aos="fade-down">Experience</div>

      <swiper
        :cssMode="true"
        :navigation="true"
        :pagination="{}"
        :mousewheel="true"
        :keyboard="{
          enabled: true,
        }"
        :modules="modules"
        class="mySwiper"
        data-aos="fade-down"
      >
        <swiper-slide v-for="(slide, index) in Slide" :key="index">
          <div class="mt-10">
            <div class="flex place-content-around">
              <img
                class="object-fill bg-cover hover:object-scale-down h-full max-h-96 max-w-[30%] pb-5"
                :src="slide.img"
                :alt="slide.name"
              />
            </div>
            <h2 class="flex place-content-around text-2xl font-semibold">
              {{ slide.name }}
            </h2>
            <div>
              <button
                class="px-4 py-2 mt-4 bg-green-200 rounded-sm hover:bg-pink-200"
                @click="openDialog(slide)"
              >
                More Details
              </button>
            </div>
            <p class="mt-4 text-xs">{{ slide.description }}</p>
          </div>
        </swiper-slide>
      </swiper>

      <!-- Dialog component -->
      <transition name="slide-fade" class=" flex text-center">
        <div v-if="dialogOpen" class="dialog -mt-60  z-10 flex flex-col place-content-around h-96  w-full">
          <div class="flex place-content-around">
            <h2>{{ selectedSlide.name }}</h2>
          </div>
        <div class="flex text-center items-center place-content-around ">
         <div class=" max-w-[20%]">
          <img :src="selectedSlide.img" alt="">
         </div>
          <p>{{ selectedSlide.description }}  <br>
            <span class=" font-bold text-xl">Technology used: </span>    {{ selectedSlide.technology}}
          </p> 
     
        </div>
          <div class=" flex place-content-between">
            <div></div>
            <button @click="closeDialog" class=" bg-red-200 hover:bg-green-200 p-2 rounded-sm" >Close</button>
          </div>
         
        </div>
      </transition>
    </div>
  </section>
</template>
<style>
.slide-fade-enter-active {
  transition: all 0.4s ease-out;
}

.slide-fade-leave-active {
  transition: all 0.3s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: translateX(20px);
  opacity: 0;
}
.dialog {
  background-color: white;
  height: 120%;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  
}
</style>
