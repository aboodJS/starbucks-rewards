<script setup>
const show = defineModel()
</script>

<template>
  <aside
    :class="[
      'grid md:hidden bg-white w-[70%] absolute h-[60vh] top-28 z-10 transition-all',
      show ? 'right-0 shadow-2xl shadow-black shadow' : '-right-80 hidden',
    ]"
  >
    <div class="grid h-1/2 mt-12">
      <ul class="grid gap-7 justify-center pb-6">
        <li>Menu</li>
        <li>Rewards</li>
        <li>Gift Cards</li>
        <hr class="w-[220px] justify-self-center" />
      </ul>
      <div class="flex justify-evenly w-3/4">
        <button class="border-[1px] p-1 px-4 rounded-4xl h-fit">Sign in</button
        ><button class="h-fit p-1 px-4 rounded-4xl text-white bg-black">Join now</button>
      </div>
    </div>
  </aside>
</template>
