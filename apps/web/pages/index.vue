<template>
  <div
    class="relative min-h-[850px] mb-0 bg-hero flex items-center justify-center w-full bg-cover bg-no-repeat bg-center flex-col"
  >
    <h5 class="text-blue-950 font-bold text-6xl mb-6 text-center">Welcome to the</h5>
    <img src="/images/Aldi_Wordmark.png" alt="Aldi" class="max-w-full block mb-6" />
    <h5 class="text-blue-950 font-bold text-6xl mb-6 text-center">Merchandise Store</h5>
    <NuxtLink
      class="bg-blue-950 text-white text-lg font-bold inline-flex justify-center items-center rounded-full py-4 px-16"
      to="#"
      >Shop Now!</NuxtLink
    >
  </div>
</template>

<script setup lang="ts">
import type { HeroProps } from '~/components/ui/Hero/types';

defineProps<HeroProps>();

const NuxtLink = resolveComponent('NuxtLink');
</script>
