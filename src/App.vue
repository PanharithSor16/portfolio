<script setup>
import Navbar from "./components/Navbar.vue";
import Hero from "./components/Hero.vue";
import AOS from "aos";
import "aos/dist/aos.css";
import { ref, onMounted } from "vue";
import About from "./components/About.vue";
// Initialize AOS when the component is mounted
onMounted(() => {
  AOS.init({
    duration: 2400
    // Global settings if needed
  });
});
</script>
<template>
  <div class=" bg-[#17202A]">
    <Hero />
    <About/>
    <Navbar />
   
  </div>
</template>
