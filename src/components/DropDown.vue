<script setup>
import { ref } from 'vue'
defineProps(['title'])
const view = ref(false)
</script>

<template>
  <ul
    :class="[
      'grid content-evenly gap-5 transition-all overflow-hidden',
      view ? 'max-md:h-fit' : 'max-md:h-7',
    ]"
  >
    <h1 class="font-semibold flex items-center" @click="() => (view = !view)">
      {{ title }}
      <div class="md:hidden">
        <i
          :class="['bx bx-chevron-down transition-transform text-2xl', view ? 'rotate-180' : '']"
        ></i>
      </div>
    </h1>
    <slot></slot>
  </ul>
</template>
