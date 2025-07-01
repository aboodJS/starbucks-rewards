<script setup>
defineProps(['image', 'title', 'unique-id'])
defineEmits(['showBox', 'change-id'])
</script>

<template>
  <main
    @click="$emit('showBox')"
    class="grid md:gap-5 max-md:grid-rows-2 max-md:grid-cols-4 max-md:justify-center max-md:gap-x-5 md:grid-cols-1 md:text-center"
  >
    <img :src="image" alt="" class="justify-self-center h-[112px] row-span-2 self-center" />

    <p
      class="font-bold w-fit md:justify-self-center max-md:text-left max-md:self-center col-span-2"
    >
      {{ title }}
    </p>
    <p
      class="md:w-1/2 max-md:text-sm justify-self-center md:text-center max-md:col-start-2 max-md:self-center col-span-2"
    >
      <slot></slot>
    </p>
    <a
      href="#"
      class="text-center text-[#006241] underline justify-self-center md:col-start-1 max-md:col-start-2"
      >learn more</a
    >
  </main>
</template>
