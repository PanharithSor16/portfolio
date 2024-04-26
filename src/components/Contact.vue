<script setup>
import { ref } from 'vue';

const name = ref('')
const email = ref('')
const message = ref('')
</script>
<template>
  <section>
    <div class="text-red-200 text-center text-2xl">Contact</div>
    <div class="block md:flex mt-5 place-content-around items-center justify-center  mb-5">
      <div class=" mt-5 bg-gray-200 rounded-lg p-4 m-2 md:w-2/4 pb-3"   data-aos="fade-up">
        <form class="text-start">
          <label class="block">Name</label>
          <input
            type="text"
            v-model="name"
            name="name"
            placeholder="Your Name"
            class="w-full px-4 py-2 border border-gray-300 rounded-lg mt-1"
          />
          <label class="block">Email</label>
          <input
            type="email"
            v-model="email"
            name="email"
            placeholder="Your Email"
            class="w-full px-4 py-2 border border-gray-300 rounded-lg mt-1"
          />
          <label class="block">Message</label>
          <textarea
            name="message"
            v-model="message"
            cols="30"
            rows="5"
            placeholder="Message"
            class="w-full px-4 py-2 border border-gray-300 rounded-lg mt-1"
          >
          </textarea>

          <input type="submit" value="Send" class="bg-green-500 text-white px-4 py-2 rounded-lg mt-4 cursor-pointer hover:bg-green-600" />
        </form>
      </div>
      <div class="text-cyan-200 sm:ml-5 block justify-center text-center items-center"   data-aos="fade-right">
        <div class="w-full items-center">
          <div>Helo I'm Panharith

        </div>
           <div class="flex place-content-around"> <img class="w-72 mt-2 self-center " src="/src/assets/image1.png" alt=""></div>
        </div>
        
      </div>
    </div>
    
  </section>
</template>
