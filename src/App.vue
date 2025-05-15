<script setup>
import NavBar from './components/NavBar.vue'
</script>

<template>
  <NavBar></NavBar>
  <section class="flex justify-evenly h-[67vh] items-center bg-[#fbf5e8]">
    <div class="grid gap-5 ml-16">
      <h1 class="text-5xl font-bold text-green-600 w-9/12">It's a great day for free coffee</h1>
      <p>Sign up and start enjoying the perks of Starbucks® Rewards.</p>
      <button
        class="bg-[#00754a] h-10 w-24 text-white rounded-3xl py-1 px-3 hover:bg-green-800 transition-colors"
      >
        Join now
      </button>
      <p>It's even better with <a href="#" class="underline">the app</a>.</p>
    </div>
    <img src="./assets/pexels-chiecharon-1193335.jpg" alt="" class="w-1/2 h-[67vh]" />
  </section>
</template>
