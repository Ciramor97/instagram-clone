<template>
  <section
    class="inset-y-0 flex flex-col justify-center absolute pointer-events-none text-white/90 font-light space-y-3 text-xs left-6"
  >
    <div class="flex space-x-4 items-center">
      <IconLetters class="text-xl"></IconLetters>
      <span>Create</span>
    </div>
    <div class="flex space-x-4 items-center">
      <IconInfinity class="text-xl"></IconInfinity>
      <span>Boomerang</span>
    </div>
    <div class="flex space-x-4 items-center">
      <IconLayout class="text-xl"></IconLayout>
      <span>Layout</span>
    </div>
    <IconChevronDown class="text-lg"></IconChevronDown>
  </section>
</template>
<script setup lang="ts">
import IconChevronDown from "~icons/tabler/chevron-down";
import IconLetters from "~icons/tabler/letter-case";
import IconInfinity from "~icons/tabler/infinity";
import IconLayout from "~icons/tabler/layout";
</script>
