<script setup>
defineProps(['number', 'title'])
</script>

<template>
  <main
    class="grid md:gap-5 max-md:grid-rows-2 max-md:grid-cols-4 max-md:justify-center max-md:gap-x-5 w-fit"
  >
    <div
      class="rounded-full text-2xl border-2 w-9 text-center md:justify-self-center max-md:row-span-2 self-center justify-self-end"
    >
      {{ number }}
    </div>
    <p class="font-bold w-fit justify-self-center max-md:text-left max-md:self-center col-span-2">
      {{ title }}
    </p>
    <p
      class="md:w-1/2 max-md:text-sm justify-self-center md:text-center max-md:col-start-2 max-md:self-center col-span-2"
    >
      <slot></slot>
    </p>
  </main>
</template>
