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
  <section id="Experience" class="relative bg-black text-white py-24 px-6 overflow-hidden">
    <!-- Top rule -->
    <div class="w-full border-t border-neutral-800 mb-16 relative">
      <span class="absolute -top-3 left-6 bg-black px-3 text-xs font-mono tracking-[0.3em] text-neutral-500 uppercase">
        &#9658;&#9658;&#9658; Experience
      </span>
    </div>

    <div class="max-w-5xl mx-auto">
      <swiper
        :cssMode="true"
        :navigation="true"
        :pagination="{ clickable: true }"
        :mousewheel="true"
        :keyboard="{ enabled: true }"
        :modules="modules"
        class="film-swiper w-full"
        data-aos="fade-up"
      >
        <swiper-slide v-for="(slide, index) in Slide" :key="index">
          <div class="flex flex-col md:flex-row items-center md:items-start gap-8 px-2 md:px-10 py-8">

            <!-- Image -->
            <div class="w-4/5 sm:w-3/5 md:w-2/5 flex-shrink-0">
              <div class="relative group">
                <img
                  class="w-full object-cover grayscale contrast-110 border border-neutral-800 max-h-64 group-hover:grayscale-0 transition-all duration-500"
                  :src="slide.img"
                  :alt="slide.name"
                />
                <!-- Film corners -->
                <div class="absolute top-0 left-0 w-4 h-4 border-t border-l border-white/50"></div>
                <div class="absolute top-0 right-0 w-4 h-4 border-t border-r border-white/50"></div>
                <div class="absolute bottom-0 left-0 w-4 h-4 border-b border-l border-white/50"></div>
                <div class="absolute bottom-0 right-0 w-4 h-4 border-b border-r border-white/50"></div>
                <!-- Frame number -->
                <span class="absolute top-1 left-1 text-[9px] font-mono text-white/40 tracking-widest">{{ String(index + 1).padStart(2, '0') }}</span>
              </div>
            </div>

            <!-- Content -->
            <div class="w-full md:w-3/5 flex flex-col items-center md:items-start text-center md:text-left">
              <p class="text-xs font-mono tracking-[0.3em] text-neutral-500 uppercase mb-2">
                &#9658; Project {{ String(index + 1).padStart(2, '0') }}
              </p>
              <h2 class="text-2xl sm:text-3xl font-bold uppercase tracking-tight" style="font-family: Georgia, serif;">
                {{ slide.name }}
              </h2>
              <p class="mt-3 text-sm text-neutral-400 leading-relaxed max-w-sm">{{ slide.description }}</p>
              <div class="mt-4 space-y-1 text-xs font-mono text-neutral-500">
                <p><span class="text-neutral-300 mr-2">TECH</span>{{ slide.technology }}</p>
                <p><span class="text-neutral-300 mr-2">ROLE</span>{{ slide.responsible }}</p>
              </div>
              <button
                class="mt-6 border border-neutral-700 hover:border-white hover:bg-white hover:text-black text-neutral-300 transition-all duration-300 px-6 py-2 text-xs tracking-[0.3em] uppercase font-mono"
                @click="openDialog(slide)"
              >
                View Details
              </button>
            </div>

          </div>
        </swiper-slide>
      </swiper>
    </div>

    <!-- Modal -->
    <transition name="slide-fade">
      <div
        v-if="dialogOpen"
        class="fixed inset-0 z-50 flex items-center justify-center bg-black/80 px-4"
        @click.self="closeDialog"
      >
        <div class="relative bg-neutral-950 border border-neutral-700 w-full max-w-lg p-8 flex flex-col gap-4">
          <!-- Film corners -->
          <div class="absolute top-0 left-0 w-5 h-5 border-t-2 border-l-2 border-white"></div>
          <div class="absolute top-0 right-0 w-5 h-5 border-t-2 border-r-2 border-white"></div>
          <div class="absolute bottom-0 left-0 w-5 h-5 border-b-2 border-l-2 border-white"></div>
          <div class="absolute bottom-0 right-0 w-5 h-5 border-b-2 border-r-2 border-white"></div>

          <p class="text-xs font-mono tracking-[0.3em] text-neutral-500 uppercase">&#9658; Details</p>
          <h2 class="text-2xl font-bold uppercase tracking-tight" style="font-family: Georgia, serif;">
            {{ selectedSlide.name }}
          </h2>
          <p class="text-sm text-neutral-400 leading-relaxed">{{ selectedSlide.description }}</p>
          <div class="space-y-1 text-xs font-mono text-neutral-500">
            <p><span class="text-neutral-300 mr-2">TECH</span>{{ selectedSlide.technology }}</p>
            <p><span class="text-neutral-300 mr-2">ROLE</span>{{ selectedSlide.responsible }}</p>
          </div>
          <div class="flex justify-between mt-2 border-t border-neutral-800 pt-4">
            <a :href="selectedSlide.demo" target="_blank"
              class="border border-neutral-700 hover:border-white hover:bg-white hover:text-black text-neutral-300 transition-all duration-300 px-5 py-2 text-xs tracking-[0.3em] uppercase font-mono">
              Demo
            </a>
            <button @click="closeDialog"
              class="border border-neutral-700 hover:border-white hover:bg-white hover:text-black text-neutral-300 transition-all duration-300 px-5 py-2 text-xs tracking-[0.3em] uppercase font-mono">
              Close
            </button>
          </div>
        </div>
      </div>
    </transition>

    <!-- Bottom rule -->
    <div class="w-full border-t border-neutral-800 mt-16"></div>
  </section>
</template>

<style>
.slide-fade-enter-active { transition: all 0.3s ease-out; }
.slide-fade-leave-active { transition: all 0.25s cubic-bezier(1, 0.5, 0.8, 1); }
.slide-fade-enter-from,
.slide-fade-leave-to { transform: translateY(16px); opacity: 0; }

.film-swiper { width: 100%; padding-bottom: 48px !important; }

.film-swiper .swiper-button-next,
.film-swiper .swiper-button-prev {
  color: white;
  width: 32px;
  height: 32px;
}
.film-swiper .swiper-button-next::after,
.film-swiper .swiper-button-prev::after {
  font-size: 16px;
  font-weight: 900;
}
.film-swiper .swiper-pagination-bullet {
  background: #555;
  opacity: 1;
}
.film-swiper .swiper-pagination-bullet-active {
  background: white;
}
</style>
