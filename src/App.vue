<script setup>
import Navbar from "./components/Navbar.vue";
import Hero from "./components/Hero.vue";
import AOS from "aos";
import "aos/dist/aos.css";
import { ref, onMounted } from "vue";
import About from "./components/About.vue";
import Skills from "./components/Skills.vue";
import Experience from "./components/Experience.vue";
import Footer from "./components/Footer.vue";
import Contact from "./components/Contact.vue";
import { RouterLink, RouterView } from "vue-router";
import ImageMe from "./components/collection/ImageMe.vue";
// Initialize AOS when the component is mounted
onMounted(() => {
  AOS.init({

      // offset: 120, // offset (in px) from the original trigger point
      // values from 0 to 3000, with step 50ms
      duration: 1800, 
      delay: 600,// values from 0 to 3000, with step 50ms
       
    // Global settings if needed
  });
});
</script>
<template>
  <!-- bg-[#17202A] -->
  <div class="lugrasimo-regular bg-pink-100 text-red-950 flex-col place-content-around">
    <Hero />
    <About />
    <Skills />
    <Experience />
    <Contact />
     <div class="z-10 mt-4 sticky">
    <Navbar />
  </div>
    <Footer />
    <!-- <ImageMe/> -->
  </div>
</template>

<style scoped>
.lugrasimo-regular {
  font-family: "Lugrasimo", cursive;
}


</style>