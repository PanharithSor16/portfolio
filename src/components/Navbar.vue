<script setup>
import { inject, ref, onMounted, onUnmounted } from 'vue';
const isDark = inject('isDark');
const toggleDark = inject('toggleDark');

const activeSection = ref('Home');
const sections = ['Home', 'About', 'Skills', 'Experience', 'Timeline', 'Contact'];

function onScroll() {
  for (const id of sections) {
    const el = document.getElementById(id);
    if (!el) continue;
    const rect = el.getBoundingClientRect();
    if (rect.top <= window.innerHeight / 2 && rect.bottom >= window.innerHeight / 2) {
      activeSection.value = id;
      break;
    }
  }
}

onMounted(() => window.addEventListener('scroll', onScroll, { passive: true }));
onUnmounted(() => window.removeEventListener('scroll', onScroll));
</script>

<template>
  <nav class="flex place-content-center z-50">
    <div
      class="fixed bottom-6 list-none flex items-center gap-1 bg-black border border-neutral-800 px-2 py-2 font-mono text-xs"
      data-aos="fade-up"
    >
      <!-- Sprocket dots left -->
      <div class="flex flex-col gap-1 mr-2 opacity-40">
        <div class="w-1.5 h-1.5 rounded-sm bg-neutral-500"></div>
        <div class="w-1.5 h-1.5 rounded-sm bg-neutral-500"></div>
      </div>

      <a
        v-for="id in sections"
        :key="id"
        :href="`#${id}`"
        class="px-3 py-1.5 tracking-[0.2em] uppercase transition-all duration-200"
        :class="activeSection === id
          ? 'bg-white text-black'
          : 'text-neutral-500 hover:text-white'"
      >
        {{ id }}
      </a>

      <!-- Divider -->
      <div class="w-px h-5 bg-neutral-800 mx-1"></div>

      <!-- Dark mode toggle -->
      <button
        @click="toggleDark"
        class="px-3 py-1.5 tracking-[0.2em] uppercase text-neutral-500 hover:text-white transition-colors duration-200"
        :title="isDark ? 'Light mode' : 'Dark mode'"
      >
        {{ isDark ? '[ L ]' : '[ D ]' }}
      </button>

      <!-- Sprocket dots right -->
      <div class="flex flex-col gap-1 ml-2 opacity-40">
        <div class="w-1.5 h-1.5 rounded-sm bg-neutral-500"></div>
        <div class="w-1.5 h-1.5 rounded-sm bg-neutral-500"></div>
      </div>
    </div>
  </nav>
</template>
