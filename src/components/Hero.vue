<script setup>
import { CoFlagKh } from "@kalimahapps/vue-icons";
</script>
<template>
  <section id="Hero">
    <div class=" items-center align-middle md:flex place-content-around">
      <div class="mt-28 items-center ">
        <div class="ml-10 md:ml-0 flex-row place-content-center items-center content-center " data-aos-duration="1200">
          <h1
            class="text-green-300 font-semibold text-2xl"
            data-aos="fade-down"
            

          >
            Hello, I'm <span class="text-red-300 text-3xl"  data-aos="fade-down"><CoFlagKh /> Panharith  </span> <br />
          </h1>

          <h1 
            class="text-gray-300 font-normal text-3xl ml-10 mt-2"
            data-aos="fade-left"
          >
            FullStack
          </h1>

          <h1
            class="text-red-100 font-normal text-3xl ml-20 mt-2"
            data-aos="fade-right"
          >
            Developer
          </h1>
          <p class="mt-5 text-green-100" data-aos="fade-up">
            I'm Software Engineering, I'm working at Marunix Cambodia in Phnom
            Penh
          </p>
          <p class="text-green-100" data-aos="fade-up">
            I'm From Kirirom Institute of Technology
          </p>
        </div>
        <button class="bg-red-200 p-2 mt-6 font-semibold ml-10 md:ml-0 rounded-md" data-aos="fade-right">
          GET CV
        </button>
        <div class="ml-10 md:ml-0 ">
          <h1 class=" text-emerald-200 text-xl mt-6 " data-aos="zoom-out">My Hobby</h1>
          <p class=" text-red-200" data-aos="zoom-in"> About Me: <span class=" text-red-100">I'm a person that like travel, Sport especially Football
            <br>and also like to find something new for my self
          </span> <br>
          <span class="mt-3">At the free Time I like read NOVEL and Anime</span>
        </p>
        </div>
      </div>

      <div class=" mt-20 text-red-100 flex items-center place-content-around mr-2">
        <div class=""> 
          <div class=" w-44 mb-3" data-aos="fade-down">
            <img src="/src/assets/image1.png" alt="">
        </div>
        <div class=" w-44" data-aos="fade-up">
          <img src="/src/assets/image2.png"  data-aos="fade-up" alt="">
        </div>
      </div>
        <div class="ml-4">
          <div class=" w-44" data-aos="flip-down">
            <img src="/src/assets/image3.png"  data-aos="flip-down" alt="">
          </div>
      
            <div class=" w-60 mt-3" data-aos="zoom-in">
              <img src="/src/assets/image4.png" data-aos="zoom-in" alt="">
            </div>
           
            <div class=" w-60 mt-3 pb-2" data-aos="fade-left">
              <img src="/src/assets/image5.png" data-aos="fade-left" alt="">
            </div>
          
        </div>
      </div>
    </div>
  </section>
</template>
