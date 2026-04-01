<script setup>
const events = [
  { year: '2020', title: 'Started at KIT', description: 'Enrolled at Kirirom Institute of Technology, beginning my journey in Software Engineering.' },
  { year: '2021', title: 'First Project', description: 'Built my first mobile application using Flutter and Firebase during the first year of study.' },
  { year: '2022', title: 'Dev Training Phase 1', description: 'Participated in Development Training Phase 1. My team achieved runner-up for best application build.' },
  { year: '2022', title: 'Dev Training Phase 2', description: 'Completed Phase 2 of Development Training, gaining deeper experience in full-stack development.' },
  { year: '2023', title: 'PromoKH Platform', description: 'Joined the PromoKH project as a Backend developer using Next.js, Spring Boot, MongoDB and AWS S3.' },
  { year: '2023', title: 'Jart Jaeng App', description: 'Developed the Jart Jaeng mobile app for online sellers using Flutter and Firebase.' },
  { year: '2024', title: 'CheckMe OUT', description: 'Built CheckMeOut, a virtual stock management app using Android SDK, FastAPI and AWS S3.' },
  { year: '2024', title: 'Machine Project', description: 'Delivered a full-stack machine tracking system using Spring Boot, Vue.js, Tailwind CSS and SQL Server.' },
  { year: '2024', title: 'Graduated', description: 'Completed Bachelor of Software Engineering at Kirirom Institute of Technology.' },
];
</script>

<template>
  <section id="Timeline" class="relative bg-neutral-950 text-white py-24 px-6 overflow-hidden">
    <!-- Top rule -->
    <div class="w-full border-t border-neutral-800 mb-16 relative">
      <span class="absolute -top-3 left-6 bg-neutral-950 px-3 text-xs font-mono tracking-[0.3em] text-neutral-500 uppercase">
        &#9658;&#9658;&#9658; Journey
      </span>
    </div>

    <div class="max-w-4xl mx-auto">

      <div class="relative">
        <!-- Vertical center line -->
        <div class="absolute left-1/2 -translate-x-px top-0 bottom-0 w-px bg-neutral-800"></div>

        <div
          v-for="(event, index) in events"
          :key="index"
          class="relative flex items-start mb-12"
          :class="index % 2 === 0 ? 'flex-row' : 'flex-row-reverse'"
          :data-aos="index % 2 === 0 ? 'fade-right' : 'fade-left'"
        >
          <!-- Card -->
          <div class="w-5/12 border border-neutral-800 bg-black hover:border-neutral-600 transition-all duration-300 hover:scale-[1.02] relative">
            <!-- Film corners -->
            <div class="absolute top-0 left-0 w-3 h-3 border-t border-l border-neutral-600"></div>
            <div class="absolute top-0 right-0 w-3 h-3 border-t border-r border-neutral-600"></div>
            <div class="absolute bottom-0 left-0 w-3 h-3 border-b border-l border-neutral-600"></div>
            <div class="absolute bottom-0 right-0 w-3 h-3 border-b border-r border-neutral-600"></div>

            <div class="border-b border-neutral-800 px-4 py-2">
              <p class="text-[10px] font-mono tracking-[0.3em] text-neutral-600 uppercase">&#9658; Event</p>
              <h3 class="text-sm font-semibold text-white uppercase tracking-wide mt-0.5">{{ event.title }}</h3>
            </div>
            <div class="px-4 py-3">
              <p class="text-xs text-neutral-400 leading-relaxed">{{ event.description }}</p>
            </div>
          </div>

          <!-- Center dot -->
          <div class="w-2/12 flex justify-center pt-4 z-10">
            <div class="w-2.5 h-2.5 rounded-full bg-neutral-800 border border-neutral-500 ring-4 ring-neutral-950"></div>
          </div>

          <!-- Year -->
          <div class="w-5/12 flex pt-3" :class="index % 2 === 0 ? 'justify-start' : 'justify-end'">
            <span class="text-xs font-mono tracking-[0.3em] text-neutral-500 px-3 py-1 border border-neutral-800">
              {{ event.year }}
            </span>
          </div>
        </div>

      </div>
    </div>

    <!-- Bottom rule -->
    <div class="w-full border-t border-neutral-800 mt-8"></div>
  </section>
</template>
