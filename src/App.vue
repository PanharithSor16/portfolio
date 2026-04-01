<script setup>
import Navbar from "./components/Navbar.vue";
import Hero from "./components/Hero.vue";
import AOS from "aos";
import "aos/dist/aos.css";
import { ref, onMounted, provide } from "vue";
import About from "./components/About.vue";
import Skills from "./components/Skills.vue";
import Experience from "./components/Experience.vue";
import Footer from "./components/Footer.vue";
import Contact from "./components/Contact.vue";
import TimeLine from "./components/TimeLine.vue";

const isDark = ref(true);
const toggleDark = () => { isDark.value = !isDark.value; };
provide('isDark', isDark);
provide('toggleDark', toggleDark);

onMounted(() => {
  AOS.init({
      duration: 1800,
      delay: 600,
  });
});
</script>
<template>
  <div :class="isDark ? 'dark' : ''">
    <div class="flex-col place-content-around bg-black text-white">
      <Hero />
      <About />
      <Skills />
      <Experience />
      <TimeLine />
      <Contact />
      <div class="z-10 mt-4 sticky">
        <Navbar />
      </div>
      <Footer />
    </div>
  </div>
</template>

<style scoped>
.lugrasimo-regular {
  font-family: "Lugrasimo", cursive;
}


</style>