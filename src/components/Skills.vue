<script setup>
import {
  VsFileTypeNode,
  VsFileTypePythowo,
  DeVuejsOriginal,
  DeJavaOriginal,
  DeFlutterOriginal,
  DeAndroidOriginal,
  DeReactOriginal,
  DePostgresqlPlain,
  DeNuxtjsOriginal,
  VsFileTypeLightNext,
  DeTailwindcssPlain,
  DeJavascriptOriginal,
} from "@kalimahapps/vue-icons";

const skills = [
  { icon: VsFileTypePythowo, name: 'Python' },
  { icon: DeVuejsOriginal,   name: 'Vue' },
  { icon: DeJavaOriginal,    name: 'Java' },
  { icon: DeReactOriginal,   name: 'React' },
  { icon: DeNuxtjsOriginal,  name: 'Nuxt.js' },
  { icon: DeTailwindcssPlain,name: 'Tailwind' },
  { icon: VsFileTypeLightNext, name: 'Next.js' },
  { icon: DeJavascriptOriginal, name: 'JavaScript' },
  { icon: DePostgresqlPlain, name: 'SQL' },
  { icon: DeFlutterOriginal, name: 'Flutter' },
  { icon: VsFileTypeNode,    name: 'Node.js' },
  { icon: DeAndroidOriginal, name: 'Android' },
];
</script>

<template>
  <section id="Skills" class="relative bg-neutral-950 text-white py-24 px-6 overflow-hidden">
    <!-- Top rule -->
    <div class="w-full border-t border-neutral-800 mb-16 relative">
      <span class="absolute -top-3 left-6 bg-neutral-950 px-3 text-xs font-mono tracking-[0.3em] text-neutral-500 uppercase">
        &#9658;&#9658;&#9658; Skills
      </span>
    </div>

    <div class="max-w-5xl mx-auto">

      <!-- Skills grid -->
      <div class="mb-20">
        <h2 class="text-xs font-mono tracking-[0.4em] text-neutral-500 uppercase mb-8" data-aos="fade-right">
          &#9658; Technologies
        </h2>
        <div class="grid grid-cols-3 sm:grid-cols-4 md:grid-cols-6 gap-px bg-neutral-800">
          <div
            v-for="(skill, i) in skills"
            :key="i"
            class="bg-neutral-950 hover:bg-neutral-800 transition-colors duration-200 flex flex-col items-center justify-center gap-2 py-6 px-2 group cursor-default"
            data-aos="fade-up"
          >
            <component :is="skill.icon" class="size-7 text-neutral-400 group-hover:text-white transition-colors duration-200" />
            <span class="text-xs font-mono text-neutral-600 group-hover:text-neutral-300 transition-colors duration-200 tracking-wider">
              {{ skill.name }}
            </span>
          </div>
        </div>
      </div>

      <!-- Development tracks -->
      <div>
        <h2 class="text-xs font-mono tracking-[0.4em] text-neutral-500 uppercase mb-8" data-aos="fade-right">
          &#9658; Development
        </h2>
        <div class="grid sm:grid-cols-2 gap-px bg-neutral-800">

          <!-- Mobile -->
          <div class="bg-neutral-950 p-0 overflow-hidden group" data-aos="fade-right">
            <div class="relative overflow-hidden">
              <img src="/src/assets/mobi_img.jpg" alt="Mobile"
                class="w-full h-48 object-cover grayscale group-hover:grayscale-0 transition-all duration-500 scale-100 group-hover:scale-105" />
              <div class="absolute inset-0 bg-black/50 group-hover:bg-black/20 transition-colors duration-500"></div>
              <div class="absolute bottom-0 left-0 right-0 p-4">
                <p class="text-xs font-mono tracking-[0.3em] text-neutral-300 uppercase">Mobile Developer</p>
              </div>
              <!-- Film corners -->
              <div class="absolute top-2 left-2 w-3 h-3 border-t border-l border-white/60"></div>
              <div class="absolute top-2 right-2 w-3 h-3 border-t border-r border-white/60"></div>
              <div class="absolute bottom-2 left-2 w-3 h-3 border-b border-l border-white/60"></div>
              <div class="absolute bottom-2 right-2 w-3 h-3 border-b border-r border-white/60"></div>
            </div>
          </div>

          <!-- Web -->
          <div class="bg-neutral-950 p-0 overflow-hidden group" data-aos="fade-left">
            <div class="relative overflow-hidden">
              <img src="/src/assets/web_img.jpg" alt="Web"
                class="w-full h-48 object-cover grayscale group-hover:grayscale-0 transition-all duration-500 scale-100 group-hover:scale-105" />
              <div class="absolute inset-0 bg-black/50 group-hover:bg-black/20 transition-colors duration-500"></div>
              <div class="absolute bottom-0 left-0 right-0 p-4">
                <p class="text-xs font-mono tracking-[0.3em] text-neutral-300 uppercase">Web Developer</p>
              </div>
              <!-- Film corners -->
              <div class="absolute top-2 left-2 w-3 h-3 border-t border-l border-white/60"></div>
              <div class="absolute top-2 right-2 w-3 h-3 border-t border-r border-white/60"></div>
              <div class="absolute bottom-2 left-2 w-3 h-3 border-b border-l border-white/60"></div>
              <div class="absolute bottom-2 right-2 w-3 h-3 border-b border-r border-white/60"></div>
            </div>
          </div>

        </div>
      </div>
    </div>

    <!-- Bottom rule -->
    <div class="w-full border-t border-neutral-800 mt-16"></div>
  </section>
</template>
