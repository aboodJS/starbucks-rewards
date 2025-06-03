<script setup>
const show = defineModel()
</script>

<template>
  <aside
    :class="[
      'grid md:hidden bg-white w-[70%] absolute h-[60vh] top-28 z-10',
      show ? 'right-0' : '-right-80',
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

<style>
aside {
  box-shadow:
    inset #dfdfdf -1px 2px 2px,
    0px 0px;
}
</style>
