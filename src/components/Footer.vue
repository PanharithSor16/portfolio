<script setup>
import { DeFacebookPlain, BsInstagram , AnOutlinedPhone, AnOutlinedLinkedin, AkGithubOutlineFill   } from "@kalimahapps/vue-icons";
</script>
<template>
  <section
    class=" sticky rounded-md bg-slate-800  flex  md:flex-row gap-4 text-white place-content-around"  data-aos="fade-down"
  >
    <div class="flex flex-col place-content-around mt-12 md:m-20">
      <div class="flex items-center text-pink-100"><DeFacebookPlain class="mr-2"/> FaceBook </div>
      <div class="flex items-center text-pink-100"><BsInstagram class="mr-2" />Instagram</div>
      <div class="flex items-center text-pink-100"><AnOutlinedPhone class="mr-2" />+855 964754496</div>
      <div class="flex items-center text-pink-100"><AnOutlinedLinkedin class="mr-2" />LinkedIn</div>
      <div class="flex items-center text-pink-100"><AkGithubOutlineFill class="mr-2" />GitHub</div>    </div>
    <div class="mt-5">
      <div>Project</div>
    </div>
    <div class="mt-5">
      <div>About</div>
    </div>
    <div class="mt-5">
      <div>Contact</div>
    </div>
    
  </section>
</template>
