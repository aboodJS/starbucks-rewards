<script setup>
import NavBar from './components/NavBar.vue'
</script>

<template>
  <NavBar></NavBar>
  <section
    class="flex min-md:justify-evenly h-[67vh] items-center bg-[#fbf5e8] max-md:grid max-md:h-fit max-md:text-center max-md:justify-center"
  >
    <div class="grid gap-5 md:ml-16 max-md:mt-6">
      <h1 class="text-5xl font-bold text-[#32462f] md:w-9/12 max-md:text-2xl">
        It's a great day for free coffee
      </h1>
      <p>Sign up and start enjoying the perks of Starbucks® Rewards.</p>
      <button
        class="bg-[#00754a] h-10 w-24 text-white rounded-3xl py-1 px-3 hover:bg-green-800 transition-colors max-md:justify-self-center max-md:hidden"
      >
        Join now
      </button>
      <button
        class="bg-[#00754a] h-10 w-24 max-md:w-36 text-white rounded-3xl py-1 px-3 hover:bg-green-800 transition-colors max-md:justify-self-center md:hidden"
      >
        Join in the app
      </button>

      <p class="max-md:hidden">It's even better with <a href="#" class="underline">the app</a>.</p>
      <p class="md:hidden"><a href="#" class="underline">or join online</a>.</p>
    </div>
    <img
      src="./assets/pexels-chiecharon-1193335.jpg"
      alt=""
      class="md:w-1/2 h-[67vh] max-md:mt-7"
    />
  </section>
</template>
