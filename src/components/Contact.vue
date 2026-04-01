<script setup>
import { ref } from 'vue';
const name = ref('');
const email = ref('');
const message = ref('');
</script>

<template>
  <section id="Contact" class="relative bg-black text-white py-24 px-6 overflow-hidden">
    <!-- Top rule -->
    <div class="w-full border-t border-neutral-800 mb-16 relative">
      <span class="absolute -top-3 left-6 bg-black px-3 text-xs font-mono tracking-[0.3em] text-neutral-500 uppercase">
        &#9658;&#9658;&#9658; Contact
      </span>
    </div>

    <div class="max-w-5xl mx-auto md:flex gap-16 items-center">

      <!-- Form -->
      <div class="flex-1 mb-12 md:mb-0" data-aos="fade-right">
        <h2 class="text-xs font-mono tracking-[0.4em] text-neutral-500 uppercase mb-8">&#9658; Send a Message</h2>
        <form class="space-y-4">
          <div>
            <label class="block text-xs font-mono tracking-[0.3em] text-neutral-500 uppercase mb-1">Name</label>
            <input
              type="text"
              v-model="name"
              placeholder="Your Name"
              class="w-full bg-neutral-950 border border-neutral-800 focus:border-neutral-500 text-white placeholder-neutral-700 px-4 py-3 text-sm font-mono outline-none transition-colors duration-200"
            />
          </div>
          <div>
            <label class="block text-xs font-mono tracking-[0.3em] text-neutral-500 uppercase mb-1">Email</label>
            <input
              type="email"
              v-model="email"
              placeholder="Your Email"
              class="w-full bg-neutral-950 border border-neutral-800 focus:border-neutral-500 text-white placeholder-neutral-700 px-4 py-3 text-sm font-mono outline-none transition-colors duration-200"
            />
          </div>
          <div>
            <label class="block text-xs font-mono tracking-[0.3em] text-neutral-500 uppercase mb-1">Message</label>
            <textarea
              v-model="message"
              rows="5"
              placeholder="Your message..."
              class="w-full bg-neutral-950 border border-neutral-800 focus:border-neutral-500 text-white placeholder-neutral-700 px-4 py-3 text-sm font-mono outline-none transition-colors duration-200 resize-none"
            ></textarea>
          </div>
          <button
            type="submit"
            class="border border-neutral-700 hover:border-white hover:bg-white hover:text-black text-neutral-300 transition-all duration-300 px-8 py-3 text-xs tracking-[0.3em] uppercase font-mono"
          >
            Send
          </button>
        </form>
      </div>

      <!-- Photo + info -->
      <div class="flex-shrink-0 text-center" data-aos="fade-left">
        <div class="relative w-56 mx-auto mb-6 group">
          <img src="/src/assets/my_photo_B.jpg" alt="Panharith"
            class="w-full object-cover grayscale border border-neutral-700 group-hover:grayscale-0 transition-all duration-500" />
          <!-- Film corners -->
          <div class="absolute top-0 left-0 w-4 h-4 border-t-2 border-l-2 border-white"></div>
          <div class="absolute top-0 right-0 w-4 h-4 border-t-2 border-r-2 border-white"></div>
          <div class="absolute bottom-0 left-0 w-4 h-4 border-b-2 border-l-2 border-white"></div>
          <div class="absolute bottom-0 right-0 w-4 h-4 border-b-2 border-r-2 border-white"></div>
        </div>
        <p class="text-xs font-mono text-neutral-500 leading-relaxed max-w-xs mx-auto">
          Open to collaborations, freelance work,<br />and happy coding competitions.
        </p>
        <div class="mt-6 space-y-2 text-xs font-mono text-neutral-600">
          <p>&#9658; github.com/PanharithSor16</p>
          <p>&#9658; Phnom Penh, Cambodia</p>
        </div>
      </div>

    </div>

    <!-- Bottom rule -->
    <div class="w-full border-t border-neutral-800 mt-16"></div>
  </section>
</template>
