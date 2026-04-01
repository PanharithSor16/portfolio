<script setup></script>
<template>
  <section id="About" class="relative bg-black text-white py-24 px-6 overflow-hidden">
    <!-- Top rule -->
    <div class="w-full border-t border-neutral-800 mb-16 relative">
      <span class="absolute -top-3 left-6 bg-black px-3 text-xs font-mono tracking-[0.3em] text-neutral-500 uppercase">
        &#9658;&#9658;&#9658; About
      </span>
    </div>

    <div class="max-w-5xl mx-auto md:flex gap-16 items-start">

      <!-- Photo -->
      <div class="flex-shrink-0 mb-10 md:mb-0" data-aos="fade-right">
        <div class="relative w-64 mx-auto md:mx-0 group">
          <img src="/src/assets/my_photo_about.jpg" alt="Panharith"
            class="w-full object-cover grayscale contrast-110 border border-neutral-700 group-hover:grayscale-0 transition-all duration-500" />
          <!-- Film frame corners -->
          <div class="absolute top-0 left-0 w-4 h-4 border-t-2 border-l-2 border-white"></div>
          <div class="absolute top-0 right-0 w-4 h-4 border-t-2 border-r-2 border-white"></div>
          <div class="absolute bottom-0 left-0 w-4 h-4 border-b-2 border-l-2 border-white"></div>
          <div class="absolute bottom-0 right-0 w-4 h-4 border-b-2 border-r-2 border-white"></div>
        </div>
        <p class="text-center text-xs font-mono text-neutral-600 mt-2 tracking-widest">PANHARITH SOR</p>
      </div>

      <!-- Content -->
      <div class="flex-1">
        <!-- Bio -->
        <div class="mb-10" data-aos="fade-left">
          <h2 class="text-xs font-mono tracking-[0.4em] text-neutral-500 uppercase mb-4">&#9658; Profile</h2>
          <p class="text-neutral-300 leading-relaxed text-sm max-w-lg">
            As a software developer with three years of experience, I thrive on creating innovative and
            user-friendly products. I'm dedicated to continuous learning and value collaboration, whether
            working independently or as part of a team. Beyond coding, I enjoy spending time with loved
            ones, traveling, and exploring new ideas.
          </p>
        </div>

        <div class="grid sm:grid-cols-2 gap-8">
          <!-- Education -->
          <div data-aos="fade-up">
            <h2 class="text-xs font-mono tracking-[0.4em] text-neutral-500 uppercase mb-4">&#9658; Education</h2>
            <div class="space-y-4">
              <div class="border-l border-neutral-700 pl-4">
                <p class="text-white text-sm font-semibold uppercase tracking-wide">Bachelor of Software Engineering</p>
                <p class="text-neutral-400 text-xs mt-1 font-mono">Kirirom Institute of Technology</p>
              </div>
              <div class="border-l border-neutral-700 pl-4">
                <p class="text-white text-sm font-semibold uppercase tracking-wide">Diploma</p>
                <p class="text-neutral-400 text-xs mt-1 font-mono">Prei Sandek High School</p>
              </div>
            </div>
          </div>

          <!-- Achievement -->
          <div data-aos="fade-up">
            <h2 class="text-xs font-mono tracking-[0.4em] text-neutral-500 uppercase mb-4">&#9658; Achievement</h2>
            <div class="border-l border-neutral-700 pl-4">
              <p class="text-white text-sm font-semibold uppercase tracking-wide">Development Training</p>
              <p class="text-neutral-400 text-xs mt-1 leading-relaxed">
                Phase 1 — Runner-up for best application build.<br />
                Phase 2 — Completed with deep full-stack experience.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Bottom rule -->
    <div class="w-full border-t border-neutral-800 mt-16"></div>
  </section>
</template>
