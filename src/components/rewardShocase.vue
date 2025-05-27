<script setup>
import { ref } from 'vue'
import first from './firstOffer.vue'

const currentTab = ref('first')

const tabs = { first }
</script>

<template>
  <main class="bg-[#f1f7f5]">
    <div class="grid gap-14">
      <h1 class="font-bold text-2xl text-center pt-7">Get your favorites for free</h1>
      <ul class="flex justify-center">
        <li class="text-2xl mx-6 cursor-pointer" @click="() => (currentTab = 'first')">
          25<i class="bx bxs-star" style="color: #cba258"></i>
        </li>
        <li class="text-2xl mx-6 cursor-pointer" @click="() => (currentTab = 'second')">
          100<i class="bx bxs-star" style="color: #cba258"></i>
        </li>
        <li class="text-2xl mx-6 cursor-pointer" @click="() => (currentTab = 'third')">
          200<i class="bx bxs-star" style="color: #cba258"></i>
        </li>
        <li class="text-2xl mx-6 cursor-pointer" @click="() => (currentTab = 'fourth')">
          300<i class="bx bxs-star" style="color: #cba258"></i>
        </li>
        <li class="text-2xl mx-6 cursor-pointer" @click="() => (currentTab = 'fifth')">
          400<i class="bx bxs-star" style="color: #cba258"></i>
        </li>
      </ul>
    </div>
    <section class="h-64 bg-[#d4e9e2] inset-shadow">
      <component :is="tabs[currentTab]"></component>
    </section>
  </main>
</template>
