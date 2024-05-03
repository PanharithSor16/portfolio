<script setup>
import {
  VsFileTypeNode ,
  VsFileTypePythowo,
  DeVuejsOriginal,
  DeJavaOriginal,
  DeFlutterOriginal,
  DeAndroidOriginal,
  DeReactOriginal,
  DePostgresqlPlain,
  DeNuxtjsOriginal,
  VsFileTypeLightNext ,
  DeTailwindcssPlain,
  DeJavascriptOriginal,
} from "@kalimahapps/vue-icons";
</script>
<template>
  <section class="flex place-content-around">
    <div class="grid  items-center pb-16 md:w-[80%]">
      <div
        class="text-2xl justify-start "
        data-aos="fade-right"
      >
        Skills
      </div>
      <div class=" grid md:flex place-content-around">
        <div class=" mb-4">
          <h2></h2>
          <div class="max-w-72 rounded-md shadow-md">
            <img class=" rounded-md drop-shadow-lg"
              src="/src//assets/dev_img.jpg"
              alt=""
            />
          </div>
        </div>
        <div
          class="grid grid-cols-2 md:grid-cols-3 place-content-around items-center font-semibold text-center"
        >
          <div
            class="flex space-x-2  text-xl items-center"
            data-aos="fade-down"
          >
            <VsFileTypePythowo class="items-center size-6" />
            <p class="text-sm">Python</p>
          </div>
          <div
            class="flex space-x-2  text-xl items-center"
            data-aos="fade-down"
          >
            <DeVuejsOriginal class="items-center size-6" />
            <p class="text-sm">Vue</p>
          </div>
          <div
            class="flex space-x-2  text-xl items-center"
            data-aos="fade-down"
          >
            <DeJavaOriginal class="items-center size-6" />
            <p class="text-sm">Java</p>
          </div>
          <div
            class="mt-5 flex space-x-2  text-xl items-center"
            data-aos="fade-left"
          >
            <DeReactOriginal class="items-center size-6" />
            <p class="text-sm">React</p>
          </div>
          <div
            class="mt-5 flex space-x-2  text-xl items-center"
            data-aos="fade-in"
          >
            <DeNuxtjsOriginal class="items-center size-6" />
            <p class="text-sm">Nuxt js</p>
          </div>
          <div
            class="mt-5 flex space-x-2  text-xl items-center"
            data-aos="fade-in"
          >
            <DeTailwindcssPlain class="items-center size-6" />
            <p class="text-sm">Tailwind</p>
          </div>
          <div
            class="mt-5 flex space-x-2  text-xl items-center"
            data-aos="fade-out"
          >
            <VsFileTypeLightNext  class="items-center size-6" />
            <p class="text-sm">Next js</p>
          </div>
          <div
            class="mt-5 flex space-x-2  text-xl items-center"
            data-aos="fade-left"
          >
            <DeJavascriptOriginal class="items-center size-6" />
            <p class="text-sm">JavaScript</p>
          </div>
          <div
            class="mt-5 flex space-x-2  text-xl items-center"
            data-aos="fade-up"
          >
            <DePostgresqlPlain class="items-center size-6" />
            <p class="text-sm">SQL</p>
          </div>
          <div
            class="mt-5 flex space-x-2  text-xl items-center"
            data-aos="fade-up"
          >
            <DeFlutterOriginal class="items-center size-6" />
            <p class="text-sm">Flutter</p>
          </div>
         
          <div
            class="mt-5 flex space-x-2  text-xl items-center"
            data-aos="fade-up"
          >
            <VsFileTypeNode  class="items-center size-6" />
            <p class="text-sm">Node js</p>
          </div>
          <div
            class="mt-5 flex space-x-2  text-xl items-center"
            data-aos="fade-up"
          >
            <DeAndroidOriginal class="items-center size-6" />
            <p class="text-sm">Android</p>
          </div>
        </div>
      </div>
      <div class="mt-6 text-2xl " data-aos="fade-right">
        Technology
      </div>
      <div class="grid md:flex place-content-around mt-5 text-center">
        <div
          class="mt-5 text-xl items-center place-content-center"
          data-aos="fade-down"
        >
          <div class=" max-w-72">
            <img class=" rounded-lg" src="/src/assets/mobi_img.jpg" alt="">
          </div>
          <p>Mobile Developer</p>
        </div>
        <div
          class="mt-5  text-xl items-center place-content-center"
          data-aos="fade-up"
        >
          <div class=" max-w-72">
            <img class=" rounded-lg" src="/src/assets/web_img.jpg" alt="">
          </div>
          <p>Web Developer</p>
        </div>
      </div>
    </div>
  </section>
</template>
