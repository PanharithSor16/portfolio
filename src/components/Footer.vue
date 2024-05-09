<script setup>
import {
  DeFacebookPlain,
  BsInstagram,
  AnOutlinedPhone,
  AnOutlinedLinkedin,
  AkGithubOutlineFill,
} from "@kalimahapps/vue-icons";
</script>
<template>
  <section
  class=" rounded-md bg-slate-800  flex-col  md:flex-row gap-4 text-white place-content-around "
   data-aos="fade-down"
  >
    
    <div  class=" flex place-content-around"
   >
      <div class="flex flex-col place-content-around mt-0 md:m-20">
        <div>Project</div>
      </div>
      <div class="mt-5">
        <div>About</div>
      </div>
      <div class="mt-5 flex flex-col place-content-around md:m-20">
        <div class="flex items-center text-pink-100">
          <DeFacebookPlain class="mr-2" /> FaceBook
        </div>
        <div class="flex items-center text-pink-100">
          <BsInstagram class="mr-2" />Instagram
        </div>
        <div class="flex items-center text-pink-100">
          <AnOutlinedPhone class="mr-2" />+855 964754496
        </div>
        <div class="flex items-center text-pink-100">
          <AnOutlinedLinkedin class="mr-2" />LinkedIn
        </div>
        <div class="flex items-center text-pink-100">
          <AkGithubOutlineFill class="mr-2" />GitHub
        </div>
      </div>
    </div>
    
    <div class=" flex place-content-around">
      <div class="  border-2 mb-10 rounded bg-red-200 w-[80%]"> 
    </div>
    </div>
    <div  class=" flex place-content-around mb-10">
      <div>
        © 2024 Panharith Sor
      </div>
     
    </div>
  </section>
</template>
