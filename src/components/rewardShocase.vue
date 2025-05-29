<script setup>
import { ref } from 'vue'
import first from './firstOffer.vue'
import second from './SecondOffer.vue'
import third from './thirdOffer.vue'
import fourth from './fourthOffer.vue'
import fifth from './fifthOffer.vue'

const currentTab = ref('first')

const tabs = { first, second, third, fourth, fifth }
</script>

<template>
  <main class="bg-[#f1f7f5]">
    <div class="grid gap-14 max-md:gap-7">
      <h1 class="font-bold text-2xl text-center pt-7">Get your favorites for free</h1>
      <ul class="flex justify-center">
        <li
          class="text-2xl md:mx-6 max-md:mx-1 cursor-pointer flex items-center"
          @click="() => (currentTab = 'first')"
        >
          25<i class="bx bxs-star" style="color: #cba258"></i>
        </li>
        <li
          class="text-2xl md:mx-6 max-md:mx-1 cursor-pointer flex items-center"
          @click="() => (currentTab = 'second')"
        >
          100<i class="bx bxs-star" style="color: #cba258"></i>
        </li>
        <li
          class="text-2xl md:mx-6 max-md:mx-1 cursor-pointer flex items-center"
          @click="() => (currentTab = 'third')"
        >
          200<i class="bx bxs-star" style="color: #cba258"></i>
        </li>
        <li
          class="text-2xl md:mx-6 max-md:mx-1 cursor-pointer flex items-center"
          @click="() => (currentTab = 'fourth')"
        >
          300<i class="bx bxs-star" style="color: #cba258"></i>
        </li>
        <li
          class="text-2xl md:mx-6 max-md:mx-1 cursor-pointer flex items-center"
          @click="() => (currentTab = 'fifth')"
        >
          400<i class="bx bxs-star" style="color: #cba258"></i>
        </li>
      </ul>
    </div>
    <section
      class="md:h-64 max-md:h-[70vh] bg-[#d4e9e2] inset-shadow grid justify-center items-center"
    >
      <div class="w-fit">
        <component :is="tabs[currentTab]"></component>
      </div>
    </section>
  </main>
</template>
