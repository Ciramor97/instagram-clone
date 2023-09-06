<template>
  <div class="flex justify-between items-center text-2xl">
    <button class="cursor-pointer" @click="router.back()">
      <Close></Close>
    </button>
    <IconLightning></IconLightning>
    <IconSettings></IconSettings>
  </div>
</template>
<script setup lang="ts">
// Icons
import Close from "~icons/tabler/X";
import IconLightning from "~icons/mdi/lightning-bolt";
import IconSettings from "~icons/tabler/settings";
import { useRouter } from "vue-router";

const router = useRouter();
</script>
