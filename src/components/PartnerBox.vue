<script setup>
defineProps(['img', 'name'])
</script>

<template>
  <main class="grid justify-center text-center gap-6">
    <img :src="img" alt="" class="h-[85px] w-[190px] justify-self-center" />
    <p class="w-3/4 justify-self-center">
      <a href="#" class="text-[#00754a] underline">link your {{ name }}</a
      ><slot></slot>
    </p>
  </main>
</template>
