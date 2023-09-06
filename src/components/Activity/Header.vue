<template>
  <header class="flex space-x-2 items-center text-xl">
    <button @click="router.back()"><IconChevronLeft /></button>
    <span>Activity</span>
  </header>
</template>

<script setup lang="ts">
import { useRouter } from "vue-router";
import IconChevronLeft from "~icons/tabler/chevron-left";

const router = useRouter();
</script>
