<template>
  <footer class="flex justify-between items-center text-2xl">
    <img
      src="../../assets/roma-dev.jpg"
      class="object-cover h-8 w-8 rounded-md border border-white"
      alt="gallery icon"
    />

    <div class="flex space-x-3 text-white/50 text-xs">
      <span>POST</span>
      <span class="text-white">STORY</span>
      <span>REEL</span>
      <span>LIVE</span>
    </div>
    <div class="bg-white/10 rounded-full p-1">
      <IconRefresh />
    </div>
  </footer>
</template>

<script setup lang="ts">
import IconRefresh from "~icons/tabler/refresh";
</script>
