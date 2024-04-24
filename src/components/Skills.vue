<script setup>
import {
  CoMobile,
  BxCodeAlt,
  VsFileTypePythowo,
  DeVuejsOriginal,
  DeJavaOriginal,
  DeFlutterOriginal,
  DeAndroidOriginal,
  DeReactOriginal,
  DePostgresqlPlain,
  DeHtml5Original,
  DeCss3Plain,
  DeTailwindcssPlain,
  DeJavascriptOriginal,
} from "@kalimahapps/vue-icons";
</script>
<template>
  <section>
    <div class="grid text-cyan-400 items-center pb-16">
      <div
        class="text-2xl justify-start ml-[5%] sm:ml-[10%]"
        data-aos="fade-right"
      >
        Skills
      </div>
      <div
        class="mt-8 grid grid-cols-3 md:grid-cols-4 place-content-around items-center ml-[10%] sm:ml-[20%]"
      >
        <div class="text-cyan-400 text-xl items-center" data-aos="fade-down">
          <VsFileTypePythowo class="items-center size-10" />
          <p>Python</p>
        </div>
        <div class="text-cyan-400 text-xl items-center" data-aos="fade-down">
          <DeVuejsOriginal class="items-center size-10" />
          <p>Vue</p>
        </div>
        <div class="text-cyan-400 text-xl items-center" data-aos="fade-down">
          <DeJavaOriginal class="items-center size-10" />
          <p>Java</p>
        </div>
        <div
          class="mt-5 text-cyan-400 text-xl items-center"
          data-aos="fade-left"
        >
          <DeReactOriginal class="items-center size-10" />
          <p>React</p>
        </div>
        <div class="mt-5 text-cyan-400 text-xl items-center" data-aos="fade-in">
          <DeHtml5Original class="items-center size-10" />
          <p>HTML</p>
        </div>
        <div class="mt-5 text-cyan-400 text-xl items-center" data-aos="fade-in">
          <DeTailwindcssPlain class="items-center size-10" />
          <p>Tailwind</p>
        </div>
        <div
          class="mt-5 text-cyan-400 text-xl items-center"
          data-aos="fade-out"
        >
          <DeCss3Plain class="items-center size-10" />
          <p>CSS</p>
        </div>
        <div
          class="mt-5 text-cyan-400 text-xl items-center"
          data-aos="fade-left"
        >
          <DeJavascriptOriginal class="items-center size-10" />
          <p>JavaScript</p>
        </div>
        <div class="mt-5 text-cyan-400 text-xl items-center" data-aos="fade-up">
          <DePostgresqlPlain class="items-center size-10" />
          <p>SQL</p>
        </div>
        <div class="mt-5 text-cyan-400 text-xl items-center" data-aos="fade-up">
          <DeFlutterOriginal class="items-center size-10" />
          <p>Flutter</p>
        </div>

        <div class="mt-5 text-cyan-400 text-xl items-center" data-aos="fade-up">
          <DeAndroidOriginal class="items-center size-10" />
          <p>Android</p>
        </div>
      </div>
      <div class="mt-6 text-2xl ml-[5%] sm:ml-[10%]" data-aos="fade-right">
        Technology
      </div>
      <div class="flex place-content-around mt-5">
        <div
          class="mt-5 text-cyan-400 text-xl items-center place-content-center"
          data-aos="fade-down"
        >
          <CoMobile class="ml-10 justify-center items-center size-10 mb-2" />
          <p>Mobile Developer</p>
        </div>
        <div
          class="mt-5 text-cyan-400 text-xl items-center place-content-center"
          data-aos="fade-up"
        >
          <BxCodeAlt class="ml-10 justify-center items-center size-10 mb-2" />
          <p>Web Developer</p>
        </div>
      </div>
    </div>
  </section>
</template>
