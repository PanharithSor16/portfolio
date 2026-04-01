<script setup>
import { CoFlagKh } from "@kalimahapps/vue-icons";
</script>

<template>
  <section id="Home" class="relative w-full min-h-screen bg-black flex items-center justify-center overflow-hidden">

    <!-- Film Strip Top -->
    <div class="absolute top-0 left-0 w-full h-14 bg-black z-20 flex items-center">
      <!-- Sprocket holes row -->
      <div class="flex items-center w-full px-2 gap-[6px]">
        <div v-for="i in 60" :key="'t'+i"
          class="w-5 h-5 min-w-[20px] rounded-[4px] bg-neutral-700 border border-neutral-600 opacity-80">
        </div>
      </div>
    </div>

    <!-- Film Strip Bottom -->
    <div class="absolute bottom-0 left-0 w-full h-14 bg-black z-20 flex items-center">
      <div class="flex items-center w-full px-2 gap-[6px]">
        <div v-for="i in 60" :key="'b'+i"
          class="w-5 h-5 min-w-[20px] rounded-[4px] bg-neutral-700 border border-neutral-600 opacity-80">
        </div>
      </div>
    </div>

    <!-- Top metadata bar -->
    <div class="absolute top-0 left-0 w-full h-14 z-30 flex items-center justify-between px-6 pointer-events-none">
      <span class="text-neutral-300 text-xs font-mono tracking-widest flex items-center gap-1">
        <span class="text-neutral-400 text-base">&#9658;&#9658;&#9658;</span> panharith.dev
      </span>
      <span class="text-neutral-300 text-xs font-mono tracking-widest flex items-center gap-1">
        <span class="text-neutral-400 text-base">&#9658;&#9658;&#9658;</span> Panharith Sor
      </span>
    </div>

    <!-- Bottom metadata bar -->
    <div class="absolute bottom-0 left-0 w-full h-14 z-30 flex items-center justify-between px-6 pointer-events-none">
      <span class="text-neutral-300 text-xs font-mono tracking-widest flex items-center gap-1">
        <span class="text-neutral-400 text-base">&#9658;&#9658;&#9658;</span> github.com/PanharithSor16
      </span>
      <span class="text-neutral-300 text-xs font-mono tracking-widest flex items-center gap-1">
        <span class="text-neutral-400 text-base">&#9658;&#9658;&#9658;</span> {{ new Date().getFullYear() }}
      </span>
    </div>

    <!-- Film frame left/right borders -->
    <div class="absolute left-0 top-14 bottom-14 w-4 bg-black z-10"></div>
    <div class="absolute right-0 top-14 bottom-14 w-4 bg-black z-10"></div>

    <!-- Background photo collage (grayscale) -->
    <div class="absolute inset-x-4 top-14 bottom-14 overflow-hidden z-0">
      <div class="relative w-full h-full">
        <!-- Left edge photo -->
        <div class="absolute left-0 top-0 h-full w-[18%] overflow-hidden">
          <img src="/src/assets/my_photo_A.jpg" alt=""
            class="w-full h-full object-cover grayscale opacity-60 scale-110" />
          <div class="absolute inset-0 bg-gradient-to-r from-transparent to-black/60"></div>
        </div>
        <!-- Right edge photo -->
        <div class="absolute right-0 top-0 h-full w-[18%] overflow-hidden">
          <img src="/src/assets/my_photo_B.jpg" alt=""
            class="w-full h-full object-cover grayscale opacity-60 scale-110" />
          <div class="absolute inset-0 bg-gradient-to-l from-transparent to-black/60"></div>
        </div>
        <!-- Center background photo -->
        <div class="absolute inset-0 overflow-hidden">
          <img src="/src/assets/my_photo_C.jpg" alt=""
            class="w-full h-full object-cover grayscale opacity-40 blur-[1px]" />
          <!-- Grain overlay -->
          <div class="absolute inset-0 bg-black/30 mix-blend-multiply"></div>
        </div>
      </div>
    </div>

    <!-- Grain texture overlay -->
    <div class="absolute inset-x-4 top-14 bottom-14 z-10 pointer-events-none"
      style="background-image: url('data:image/svg+xml,%3Csvg viewBox=%220 0 200 200%22 xmlns=%22http://www.w3.org/2000/svg%22%3E%3Cfilter id=%22noise%22%3E%3CfeTurbulence type=%22fractalNoise%22 baseFrequency=%220.9%22 numOctaves=%224%22 stitchTiles=%22stitch%22/%3E%3C/filter%3E%3Crect width=%22100%25%22 height=%22100%25%22 filter=%22url(%23noise)%22 opacity=%220.08%22/%3E%3C/svg%3E');
      background-size: 200px 200px; opacity: 0.5;">
    </div>

    <!-- Center Content -->
    <div class="relative z-20 flex flex-col items-center justify-center text-center px-4 select-none">
      <!-- Main title -->
      <h1 class="leading-none text-white" style="font-family: 'Georgia', 'Times New Roman', serif;">
        <span class="block font-black uppercase tracking-tight"
          style="font-size: clamp(4rem, 14vw, 11rem); letter-spacing: -0.02em;">
          PORT
        </span>
        <span class="block italic font-light -mt-6 md:-mt-10"
          style="font-size: clamp(4.5rem, 16vw, 13rem); letter-spacing: -0.01em; line-height: 0.85;">
          folio
        </span>
      </h1>

      <!-- Name -->
      <p class="mt-4 md:mt-6 text-white italic font-semibold tracking-widest"
        style="font-family: 'Georgia', serif; font-size: clamp(1.1rem, 3vw, 1.8rem);">
        <CoFlagKh class="inline mr-2 opacity-80" />
        Panharith Sor
      </p>

      <!-- Subtitle -->
      <p class="mt-2 text-neutral-400 text-xs md:text-sm tracking-[0.3em] uppercase font-mono">
        Software Engineer &nbsp;&bull;&nbsp; KIT
      </p>

      <!-- CTA -->
      <a href="#About"
        class="mt-8 md:mt-10 inline-block border border-neutral-500 text-neutral-300 hover:bg-white hover:text-black transition-all duration-300 px-8 py-2 text-xs tracking-[0.3em] uppercase font-mono">
        View Work
      </a>
    </div>

  </section>
</template>

<style scoped>
section {
  font-synthesis: none;
}
</style>
