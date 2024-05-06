<script setup>
import {ref} from 'vue'
import { CoFlagKh } from "@kalimahapps/vue-icons";
import VueTypewriterEffect from "vue-typewriter-effect";
const Day = ref(false)
</script>
<template>
  <section id="Hero" class="flex place-content-around">
    <div class=" items-center align-middle md:flex place-content-around md:w-[80%]">
      <div v-if="Day">he</div>
      <div class="mt-0 items-center ">
        <div class="ml-10 md:ml-0 flex-row place-content-center items-center content-center" data-aos-duration="1200">
          <h1
            class=" font-semibold text-2xl"
            data-aos="fade-down"
          >
            Hello, I'm <span class=" text-3xl  hover:text-green-900 hover:bg-slate-200 "  data-aos="fade-down"><CoFlagKh /><vue-typewriter-effect :strings="['Panharith Sor', 'Software Engineer']" /> </span> <br />
          </h1>

          <p class="mt-5" data-aos="fade-up">
            I'm Software Engineering, I'm working independently
          </p>
          <p class=" hover:text-yellow-900" data-aos="fade-up">
            I'm From Kirirom Institute of Technology
          </p>
        </div>
        <button class="bg-red-200 p-2 mt-6 font-semibold ml-10 md:ml-0 rounded-md hover:pl-2 hover:ml-2" data-aos="fade-right">
          GET CV
        </button>
        <div class="ml-10 md:ml-0 ">
          <h1 class="  text-xl mt-6  hover:mb-1 " data-aos="zoom-out">My Hobby</h1>
          <p class=" " data-aos="zoom-in"> About Me: <span class="">I'm a person that like travel, Sport especially Football
            <br>and also like to find something new for my self
          </span> <br>
          <span class="mt-3">At the free Time I like read NOVEL and Anime</span>
        </p>
        </div>
      </div>

      <div class=" mt-20 text-red-100 flex items-center place-content-around mr-2">
        <div class=""> 
          <div class=" max-w-44 mb-3 shadow-sm" data-aos="fade-down">
            <img class="" src="/src/assets/image1.png" alt="">
        </div>
        <div class=" max-w-44" data-aos="fade-up">
          <img src="/src/assets/image2.png"  data-aos="fade-up" alt="">
        </div>
      </div>
        <div class="ml-4">
          <div class=" max-w-44" data-aos="flip-down">
            <img src="/src/assets/image3.png"  data-aos="flip-down" alt="">
          </div>
            <div class=" max-w-60 mt-3" data-aos="zoom-in">
              <img src="/src/assets/image4.png" data-aos="zoom-in" data-aos-easing="ease-in" alt="">
            </div>
           
            <div class=" max-w-60 mt-3 pb-2" data-aos="fade-left">
              <img src="/src/assets/image5.png" data-aos="fade-left" data-aos-once="false" alt="">
            </div>
        </div>
      </div>
    </div>
  </section>
</template>
