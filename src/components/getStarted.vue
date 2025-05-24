<script setup>
const props = defineProps(['number', 'title'])
</script>

<template>
  <main class="grid gap-5">
    <div class="rounded-full text-2xl border-2 w-9 text-center justify-self-center">
      {{ number }}
    </div>
    <p class="font-bold w-fit justify-self-center">{{ title }}</p>
    <p class="w-1/2 justify-self-center text-center"><slot></slot></p>
  </main>
</template>
